<script>
    import { onMount } from 'svelte';
    import * as pdfjsLib from 'pdfjs-dist';
    import 'pdfjs-dist/build/pdf.worker.entry';
  
    export let pdfUrl = '';
  
    onMount(async () => {
      const loadingTask = pdfjsLib.getDocument(pdfUrl);
      try {
        const pdf = await loadingTask.promise;
        console.log('PDF loaded');
  
        // Assuming you want to render the first page for simplicity
        const pageNumber = 1;
        const page = await pdf.getPage(pageNumber);
  
        const scale = 1.5;
        const viewport = page.getViewport({ scale });
        const canvasElement = document.getElementById('pdf-canvas');
        let context = null;
        if (canvasElement && canvasElement instanceof HTMLCanvasElement) {
          const context = canvasElement.getContext('2d');
          if (context) {
            canvasElement.height = viewport.height;
            canvasElement.width = viewport.width;
          }
        }

        if (context) {
          const renderContext = {
            canvasContext: context,
            viewport: viewport,
          };
          await page.render(renderContext).promise;
          console.log('Page rendered');
        }
      } catch (error) {
        console.error('Error loading PDF: ', error);
      }
    });
  </script>
  
  <canvas id="pdf-canvas"></canvas>