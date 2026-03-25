# minecraft<div style="text-align: center; background-color: #1a1a1a; padding: 20px; border-radius: 10px;">
    <h2 style="color: white; font-family: sans-serif;">Minecraft 1.12.2</h2>
    <button id="launch-button" style="padding: 15px 30px; background-color: #388e3c; color: white; border: none; border-radius: 5px; cursor: pointer; font-size: 18px; font-weight: bold; box-shadow: 0 4px #2e7d32;">
        JUGAR EN ABOUT:BLANK ⛏️
    </button>
    <p style="color: #aaa; font-family: sans-serif; font-size: 12px; margin-top: 10px;">(Se abrirá en una pestaña limpia para evitar bloqueos)</p>
</div>

<script>
document.getElementById('launch-button').onclick = function() {
    // Definimos el contenido HTML completo del juego
    const gameCode = `
<!DOCTYPE html>
<html style="width:100%;height:100%;background-color:black;">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0">
    <title>Minecraft 1.12.2 (Cloaked)</title>
    <script type="text/javascript">
        window.disableUserscripts = true;
        window.__eaglercraftLoaderClient = {
            container: "game_frame",
            name: "Eaglercraft 1.12",
            file: "net.peytonplayz585.eaglercraft.v1_12.client",
            cid: "bafybeidrnchyech7b26rqhm3tayt7p6mxvl23lzd4f5mcyqda7hbrzyal4",
            path: "",
            download: "https://cdn.jsdelivr.net/gh/genizy/mc@main/data/1.12.2.gz",
            dlSize: 15601341,
            gzip: true
        };
    <\/script>
    <script type="text/javascript" src="https://cdn.jsdelivr.net/gh/genizy/mc@main/shared/loader.js"><\/script>
    <link type="image/png" rel="shortcut icon" href="https://cdn.jsdelivr.net/gh/genizy/mc@main/shared/game.png" />
    <style>
        body, html { margin: 0; padding: 0; height: 100%; width: 100%; overflow: hidden; background-color: black; }
        #game_frame { width: 100vw; height: 100vh; }
    </style>
</head>
<body>
    <div id="game_frame"></div>
</body>
</html>`;

    // Abrimos la pestaña about:blank
    const win = window.open('about:blank', '_blank');
    
    // Escribimos el código del juego en la nueva pestaña
    win.document.open();
    win.document.write(gameCode);
    win.document.close();
};
</script>
