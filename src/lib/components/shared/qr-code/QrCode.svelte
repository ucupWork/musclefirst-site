<script lang="ts">
    import { onMount } from 'svelte';
      
    export let codeValue: string;
    export let squareSize: number; 
      
    let qrcode: any;
              
    onMount(() => {

        let script = document.createElement('script');
        script.src = "https://cdn.rawgit.com/davidshimjs/qrcodejs/gh-pages/qrcode.min.js"
        document.head.append(script);
    
        script.onload = function() {
            qrcode = new QRCode("qrcode", {
                    text: codeValue,
                    width: squareSize,
                    height: squareSize,
                    colorDark : "#000000",
                    colorLight : "#ffffff",
                    correctLevel : QRCode.CorrectLevel.H
            });		
        };				
    
    });
  </script>
  
  <style>
    #qrcode {
      margin-top:2px;
    }
  </style>
  
  <div id="qrcode" class="w-auto h-auto"></div>
  
  