# site-mario

<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Mukta:wght@300;700&display=swap" rel="stylesheet">
    <title>Super Mario</title>
</head>

<body>

    <div class="caixa-video-mario">
        <video src="video.mp4" autoplay muted loop></video>
        <div class="mascara-video"></div>
    </div>

    <div class="caixa-principal">
        <img src="logo.png" alt="logo do super mario" class="logo-mario">
        <p>Encanadores Mario & Luigi - Resolvendo Seus Problemas Com Estilo!</p>
        <p>Você já se encontrou em uma situação de emergência com encanamento? Vazamentos inesperados, canos entupidos
            ou torneiras que não param de pingar? Não se preocupe, porque estamos aqui para salvar o dia! Apresentamos a
            vocês os encanadores mais famosos do Reino dos Cogumelos - Mario e Luigi!</p>
        <button onclick="cliqueiNoBotao()">Fale conosco</button>
    </div>

    <img src="mario.png" alt="logo mario e luigi" class="imagem-mario-luigi">

    <form class="fale-conosco">
        <input placeholder="Seu nome" type="text">
        <input placeholder="Seu telefone" type="tel">
        <textarea placeholder="Digite seu problema aqui"></textarea>
        <button onclick="sumirFormulario()">Enviar formulário</button>
    </form>

    <div class="mascara-form"></div>
</body>
<script>
    let formulario = document.querySelector(".fale-conosco")
    let mascara = document.querySelector(".mascara-form")


    function cliqueiNoBotao(){
        formulario.style.left = "700px"
        mascara.style.visibility = "visible"
    }

    function sumirFormulario(){
        formulario.style.left = "-320px"
        mascara.style.visibility = "hidden"
    }

</script>

</html>


* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Mukta', sans-serif;
}


body {
    display: flex;
    height: 100vh;
    align-items: center;
    justify-content: space-evenly;
}

.logo-mario {
    width: 300px;
}

.imagem-mario-luigi {
    height: 600px;
}

.caixa-principal {
    width: 40%;
}

.caixa-video-mario {
    position: fixed;
    top: 0;
    z-index: -1;
    width: 100%;
    height: 100%;
}
video {
    position: fixed;
    top: 0;
    min-height: 100%;
    min-width: 100%;
}

.mascara-video {
    height: 100%;
    width: 100%;
    position: fixed;
    top: 0;
    background: linear-gradient(109deg, rgba(10, 12, 16, 0.99) 15%, rgba(10, 12, 16, 0.7) 50%, rgba(10, 12, 16, 0.99) 85%);
}

p {
    color: white;
    margin-top: 10px;
    font-size: 24px;
}

button {
    height: 40px;
    width: 200px;
    background: #C51111;
    border: none;
    border-radius: 4px;
    color: #fff;
    margin-top: 20px;
    cursor: pointer;
}

.fale-conosco {
    background: #fff;
    display: flex;
    flex-direction: column;
    padding: 20px;
    border-radius: 10px;
    gap: 20px;
    position: fixed;
    left: -320px;
    transition: left 1s linear;
    z-index: 4;
}

input {
    height: 40px;
    border-radius: 3px;
    border: 1px solid gray;
    padding-left: 10px;
    outline-color: chartreuse;
}

textarea {
    height: 90px;
    width: 300px;
    border-radius: 3px;
    border: 1px solid gray;
    padding: 10px;
    outline-color: chartreuse;
}

.mascara-form {
    visibility: hidden;
    height: 100vh;
    width: 100vw;
    position: fixed;
    top: 0;
    z-index: 3;
    background: linear-gradient(109deg, rgba(10, 12, 16, 0.99) 15%, rgba(10, 12, 16, 0.7) 50%, rgba(10, 12, 16, 0.99) 85%);
}
