<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=30&duration=4000&pause=1000&color=38BCBA&center=true&vCenter=true&width=600&lines=Hola+%F0%9F%91%8B+Soy+[Tu+Nombre];Desarrollador+Web;Apasionado+por+la+Tecnolog%C3%ADa;Y+World+of+Warcraft+%F0%9F%8F%81" alt="Texto animado" />
</p>

 [![Matrix SVG](https://raw.githubusercontent.com/rodrigograca31/rodrigograca31/master/matrix.svg)](https://www.youtube.com/watch?v=SDkAGkd4NLc) 

<p align="center">
  <strong>LOK'TAR OGAR! VICTORY OR DEATH!</strong>
</p>
 
<p align="center">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Escudo-React-61DAFB?style=for-the-badge&logo=react&logoColor=white&labelColor=000000" />
</p>


<h3 align="center">
  🏰 Bienvenido a mi Reino de Código 🏰
</h3>
 

<p align="center">
  <strong>⚔️ Mi equipamiento de desarrollo:</strong>
</p>

<p align="center">
  • <strong>Espada Principal:</strong> JavaScript<br/>
  • <strong>Escudo Defensivo:</strong> HTML xD<br/>
  • <strong>Armadura:</strong> React + CSS<br/>
  • <strong>Hechizos:</strong> Node.js y Express
</p>

 
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Matriz de Progreso con Ecualizador</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background-color: #0d1117;
            color: #c9d1d9;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 20px;
        }
        .container {
            background-color: #161b22;
            border-radius: 10px;
            padding: 25px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
            max-width: 1000px;
            width: 100%;
        }
        h1 {
            color: #58a6ff;
            text-align: center;
            margin-top: 0;
        }
        .matrix-container {
            overflow-x: auto;
            margin: 30px 0;
        }
        .matrix {
            display: inline-block;
            border: 1px solid #30363d;
            border-radius: 6px;
            padding: 15px;
            background-color: #0d1117;
        }
        .months {
            display: flex;
            margin-left: 60px;
        }
        .month {
            width: 20px;
            text-align: center;
            font-size: 12px;
            margin: 0 2px;
            color: #8b949e;
        }
        .days {
            display: flex;
            margin-top: 10px;
        }
        .day-labels {
            display: flex;
            flex-direction: column;
            margin-right: 10px;
            color: #8b949e;
            font-size: 12px;
        }
        .day-label {
            height: 15px;
            margin: 2px 0;
            text-align: right;
            padding-right: 5px;
        }
        .grid {
            display: flex;
            flex-direction: column;
        }
        .row {
            display: flex;
        }
        .cell {
            width: 15px;
            height: 15px;
            margin: 2px;
            border-radius: 3px;
            background-color: #161b22;
            transition: background-color 0.3s ease;
        }
        .legend {
            display: flex;
            align-items: center;
            justify-content: flex-end;
            margin-top: 15px;
            font-size: 12px;
            color: #8b949e;
        }
        .legend-text {
            margin: 0 10px;
        }
        .legend-cells {
            display: flex;
        }
        .legend-cell {
            width: 15px;
            height: 15px;
            margin: 0 2px;
            border-radius: 3px;
        }
        .controls {
            display: flex;
            justify-content: center;
            margin-top: 20px;
            gap: 15px;
        }
        button {
            background-color: #238636;
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 6px;
            cursor: pointer;
            font-weight: 500;
            transition: background-color 0.2s;
        }
        button:hover {
            background-color: #2ea043;
        }
        .info {
            margin-top: 20px;
            font-size: 14px;
            text-align: center;
            color: #8b949e;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Matriz de Progreso con Efecto de Ecualizador</h1>
        
        <div class="matrix-container">
            <div class="matrix">
                <div class="months">
                    <div class="month">Sep</div>
                    <div class="month">Oct</div>
                    <div class="month">Nov</div>
                    <div class="month">Dec</div>
                    <div class="month">Jan</div>
                    <div class="month">Feb</div>
                    <div class="month">Mar</div>
                    <div class="month">Apr</div>
                    <div class="month">May</div>
                    <div class="month">Jun</div>
                    <div class="month">Jul</div>
                    <div class="month">Aug</div>
                </div>
                
                <div class="days">
                    <div class="day-labels">
                        <div class="day-label">Mon</div>
                        <div class="day-label"></div>
                        <div class="day-label">Wed</div>
                        <div class="day-label"></div>
                        <div class="day-label">Fri</div>
                        <div class="day-label"></div>
                        <div class="day-label"></div>
                    </div>
                    
                    <div class="grid" id="grid">
                        <!-- Las celdas se generarán con JavaScript -->
                    </div>
                </div>
            </div>
        </div>
        
        <div class="legend">
            <div class="legend-text">Less</div>
            <div class="legend-cells">
                <div class="legend-cell" style="background-color: #161b22"></div>
                <div class="legend-cell" style="background-color: #0e4429"></div>
                <div class="legend-cell" style="background-color: #006d32"></div>
                <div class="legend-cell" style="background-color: #26a641"></div>
                <div class="legend-cell" style="background-color: #39d353"></div>
            </div>
            <div class="legend-text">More</div>
        </div>
        
        <div class="controls">
            <button id="startBtn">Iniciar Animación</button>
            <button id="stopBtn">Detener Animación</button>
        </div>
        
        <div class="info">
            <p>Learn how we count contributions</p>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const grid = document.getElementById('grid');
            const rows = 7;
            const cols = 52; // 52 semanas en un año
            
            // Colores de intensidad (igual que GitHub)
            const colors = [
                '#161b22',
                '#0e4429',
                '#006d32',
                '#26a641',
                '#39d353'
            ];
            
            // Crear la matriz
            for (let i = 0; i < rows; i++) {
                const row = document.createElement('div');
                row.className = 'row';
                
                for (let j = 0; j < cols; j++) {
                    const cell = document.createElement('div');
                    cell.className = 'cell';
                    // Color inicial
                    cell.style.backgroundColor = colors[0];
                    row.appendChild(cell);
                }
                
                grid.appendChild(row);
            }
            
            let animationInterval;
            
            // Función para animar las celdas como un ecualizador
            function startAnimation() {
                stopAnimation(); // Asegurarse de que no hay otra animación en curso
                
                animationInterval = setInterval(() => {
                    const cells = document.querySelectorAll('.cell');
                    
                    cells.forEach(cell => {
                        // Mayor probabilidad de celdas con baja intensidad
                        const rand = Math.random();
                        let intensity;
                        
                        if (rand < 0.6) {
                            intensity = 0; // 60% de probabilidad - sin contribución
                        } else if (rand < 0.8) {
                            intensity = 1; // 20% de probabilidad - baja contribución
                        } else if (rand < 0.9) {
                            intensity = 2; // 10% de probabilidad - contribución media
                        } else if (rand < 0.95) {
                            intensity = 3; // 5% de probabilidad - contribución alta
                        } else {
                            intensity = 4; // 5% de probabilidad - contribución muy alta
                        }
                        
                        cell.style.backgroundColor = colors[intensity];
                    });
                }, 1000); // Actualizar cada segundo
            }
            
            function stopAnimation() {
                if (animationInterval) {
                    clearInterval(animationInterval);
                }
            }
            
            // Event listeners para los botones
            document.getElementById('startBtn').addEventListener('click', startAnimation);
            document.getElementById('stopBtn').addEventListener('click', stopAnimation);
            
            // Iniciar animación automáticamente
            startAnimation();
        });
    </script>
</body>
</html>
