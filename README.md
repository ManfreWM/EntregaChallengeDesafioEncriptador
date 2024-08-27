<h1>Reto de Challenger</h1>
  En mi trabajo realizado he aplicando toda la información impartida en los cursos de principiante de programacion
  Utilice funciones, pero quise mostrar la imagen del muñeco a traves de un div
  Espero seguir aprendiendo más de este mundo fantástico de la programación

  Comparto el código del botón desencriptar:
function botonDesencriptarTexto(){
    
    let desencriptarTextoCopiado = document.getElementById('textarea_Ingreso').value;
    if (desencriptarTextoCopiado===""){
        alert("ingrese datos para Desencriptar")
    }
        textoEncriptado = desencriptarTextoCopiado
            .replace(/enter/g, 'e' )
            .replace(/imes/g, "i")
            .replace(/ai/g, "a")
            .replace(/ober/g, "o")
            .replace(/ufat/g, "u");
        console.log(textoEncriptado);
        const divContenedorMuñeco = document.getElementById('div_Resultado_Encriptado')
        divContenedorMuñeco.style.backgroundImage="none";
        divContenedorMuñeco.style.display="flex";
        divContenedorMuñeco.style.justifyContent  ="Space-around";
        divContenedorMuñeco.style.alignItems = 'center';
        divContenedorMuñeco.style.padding  = '10px';
        divContenedorMuñeco.textContent=textContent=textoEncriptado;
        document.querySelector("#textarea_Ingreso").value ="";
        document.querySelector('#botonEncriptar').removeAttribute("disabled");
        document.querySelector('#botonEncriptar').style.cursor="pointer";
        document.querySelector("#botonCopiar").style.display="none";
             
        document.querySelector('#botonDesencriptar').addEventListener('click', function() {
            setTimeout(function() {
                window.location.href="index.html";
            }, 10000); // 5000 milisegundos = 2 segundos
        });
    return;
}
