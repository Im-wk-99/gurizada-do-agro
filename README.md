/* NEBULA OS | CORE STYLESHEET v4.0 
   Paleta: Deep Black, Electric Purple, Neon Green
*/

:root {
    --purple: #bc13fe;
    --green: #20ff88;
    --bg: #030005;
    --surface: rgba(10, 5, 20, 0.7);
    --border: rgba(188, 19, 254, 0.4);
    --text: #e0d0ff;
    --shadow: 0 20px 60px rgba(0, 0, 0, 0.9);
}

/* Reset e Estrutura Base */
* { 
    margin: 0; 
    padding: 0; 
    box-sizing: border-box; 
    font-family: 'Outfit', sans-serif; 
}

body { 
    background: var(--bg);
    color: var(--text); 
    height: 100vh; 
    display: flex; 
    overflow: hidden;
}

/* Camadas de Fundo Dinâmico */
#bg-layer {
    position: fixed; 
    top: 0; 
    left: 0; 
    width: 100%; 
    height: 100%;
    z-index: -2; 
    background-size: cover; 
    background-position: center;
    transition: background-image 1.2s cubic-bezier(0.4, 0, 0.2, 1);
    filter: brightness(0.25) saturate(1.2) contrast(1.1);
}

#bg-overlay {
    position: fixed; 
    top: 0; 
    left: 0; 
    width: 100%; 
    height: 100%;
    z-index: -1; 
    background: radial-gradient(circle at center, transparent, var(--bg) 90%);
}

/* Sidebar Flutuante */
aside { 
    width: 100px; 
    background: var(--surface); 
    backdrop-filter: blur(40px);
    -webkit-backdrop-filter: blur(40px);
    border: 1px solid var(--border); 
    margin: 25px; 
    border-radius: 30px;
    display: flex; 
    flex-direction: column; 
    align-items: center; 
    padding: 35px 0;
    transition: width 0.5s cubic-bezier(0.075, 0.82, 0.165, 1); 
    z-index: 100;
    box-shadow: var(--shadow);
}

aside:hover { 
    width: 280px; 
    border-color: var(--purple); 
}

.logo-box {
    width: 55px; 
    height: 55px; 
    background: linear-gradient(135deg, var(--purple), #6a00ff);
    border-radius: 18px; 
    display: grid; 
    place-items: center;
    box-shadow: 0 0 30px rgba(188, 19, 254, 0.7); 
    margin-bottom: 50px;
}

/* Itens de Navegação */
.nav-item {
    width: calc(100% - 30px); 
    padding: 18px; 
    margin: 8px 0; 
    border-radius: 20px;
    display: flex; 
    align-items: center; 
    gap: 25px; 
    cursor: pointer; 
    transition: 0.4s;
    color: var(--text); 
    overflow: hidden; 
    position: relative;
}

.nav-item i { 
    font-size: 1.5rem; 
    min-width: 35px; 
    text-align: center; 
}

.nav-item span { 
    opacity: 0; 
    font-weight: 600; 
    white-space: nowrap; 
    letter-spacing: 1px; 
}

aside:hover .nav-item span { 
    opacity: 1; 
}

.nav-item:hover { 
    background: rgba(188, 19, 254, 0.25); 
    color: var(--green); 
}

.nav-item.active { 
    background: var(--purple); 
    color: #fff; 
    box-shadow: 0 0 35px rgba(188, 19, 254, 0.6); 
}

/* Área Principal */
main { 
    flex: 1; 
    padding: 30px 50px 30px 10px; 
    display: flex; 
    flex-direction: column; 
    overflow-y: auto; 
}

header { 
    display: flex; 
    justify-content: space-between; 
    align-items: center; 
    margin-bottom: 40px; 
}

/* Cards com Glassmorphism */
.card {
    background: var(--surface); 
    border: 1px solid var(--border); 
    border-radius: 35px;
    padding: 35px; 
    backdrop-filter: blur(25px); 
    box-shadow: var(--shadow);
    transition: 0.5s; 
    animation: slideUp 0.8s ease-out;
    position: relative; 
    overflow: hidden;
}

.card::before { 
    content: ""; 
    position: absolute; 
    top: 0; left: 0; 
    width: 100%; 
    height: 5px; 
    background: linear-gradient(90deg, transparent, var(--purple), transparent); 
    opacity: 0.5; 
}

.card:hover { 
    border-color: var(--green); 
    transform: translateY(-8px); 
}

/* Tipografia Neon */
.neon-text { 
    color: var(--green); 
    text-shadow: 0 0 20px rgba(32, 255, 136, 0.7); 
    font-weight: 900; 
}

/* Formulários Futuristas */
input, select {
    width: 100%; 
    background: rgba(0,0,0,0.7); 
    border: 1px solid var(--border);
    padding: 18px; 
    border-radius: 18px; 
    color: #fff; 
    margin-top: 12px; 
    font-weight: 600; 
    outline: none;
}

input:focus { 
    border-color: var(--green); 
    box-shadow: 0 0 15px rgba(32, 255, 136, 0.2); 
}

/* Botões de Alta Performance */
.btn-action {
    background: linear-gradient(90deg, var(--purple), #8a2be2);
    color: #fff; 
    border: none; 
    padding: 20px; 
    border-radius: 20px;
    font-weight: 900; 
    cursor: pointer; 
    margin-top: 25px; 
    width: 100%;
    text-transform: uppercase; 
    letter-spacing: 2px; 
    transition: 0.4s;
}

.btn-action:hover { 
    box-shadow: 0 0 50px var(--purple); 
    transform: scale(1.03); 
}

/* Terminal de IA */
.terminal {
    background: rgba(0,0,0,0.8); 
    border-radius: 25px; 
    padding: 25px;
    font-family: 'Courier New', monospace; 
    font-size: 0.9rem; 
    color: var(--green);
    height: 220px; 
    overflow-y: auto; 
    border: 1px solid var(--border);
}

/* Tabelas de Dados */
table { 
    width: 100%; 
    border-collapse: separate; 
    border-spacing: 0 12px; 
}

th { 
    text-align: left; 
    padding: 15px; 
    color: var(--purple); 
    font-weight: 900; 
    font-size: 0.85rem; 
}

td { 
    padding: 20px 15px; 
    background: rgba(255,255,255,0.03); 
    border-top: 1px solid rgba(188, 19, 254, 0.1); 
    border-bottom: 1px solid rgba(188, 19, 254, 0.1); 
}

td:first-child { 
    border-radius: 15px 0 0 15px; 
    border-left: 1px solid rgba(188, 19, 254, 0.1); 
}

td:last-child { 
    border-radius: 0 15px 15px 0; 
    border-right: 1px solid rgba(188, 19, 254, 0.1); 
}

/* Animações e Scroll */
@keyframes slideUp { 
    from { opacity: 0; transform: translateY(40px); } 
    to { opacity: 1; transform: translateY(0); } 
}

::-webkit-scrollbar { 
    width: 8px; 
}

::-webkit-scrollbar-thumb { 
    background: var(--purple); 
    border-radius: 10px; 
}