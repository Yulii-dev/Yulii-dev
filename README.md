<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VULIANYS BANQUEZ | README</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
        }

        :root {
            --primary: #2d3436;
            --secondary: #636e72;
            --accent: #0984e3;
            --light: #f9f9f9;
            --card-bg: #ffffff;
            --shadow: 0 8px 30px rgba(0, 0, 0, 0.08);
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            color: var(--primary);
            line-height: 1.6;
            padding: 20px;
            min-height: 100vh;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            animation: fadeIn 1s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .header {
            background: var(--card-bg);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: var(--shadow);
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, var(--accent), #00cec9);
        }

        .name {
            font-size: 2.8rem;
            font-weight: 800;
            margin-bottom: 5px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .username {
            font-size: 1.4rem;
            color: var(--secondary);
            margin-bottom: 20px;
            display: block;
        }

        .tagline {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 25px;
            color: var(--secondary);
        }

        .highlight {
            color: var(--accent);
            font-weight: 600;
        }

        .tech-icons {
            display: flex;
            justify-content: center;
            gap: 25px;
            margin: 25px 0;
            flex-wrap: wrap;
        }

        .tech-icons i {
            font-size: 2.2rem;
            color: var(--primary);
            transition: all 0.3s ease;
        }

        .tech-icons i:hover {
            color: var(--accent);
            transform: translateY(-5px);
        }

        .content-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-bottom: 30px;
        }

        .card {
            background: var(--card-bg);
            border-radius: 18px;
            padding: 30px;
            box-shadow: var(--shadow);
            transition: transform 0.3s ease;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card-title {
            font-size: 1.5rem;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #f1f1f1;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .card-title i {
            color: var(--accent);
        }

        .info-item {
            margin-bottom: 15px;
            display: flex;
            align-items: flex-start;
        }

        .info-label {
            font-weight: 600;
            min-width: 180px;
            color: var(--primary);
        }

        .info-value {
            color: var(--secondary);
            flex: 1;
        }

        .link {
            color: var(--accent);
            text-decoration: none;
            transition: all 0.2s;
            word-break: break-all;
        }

        .link:hover {
            text-decoration: underline;
        }

        .contribution-graph {
            background: #f8f9fa;
            border-radius: 12px;
            padding: 20px;
            margin-top: 15px;
        }

        .graph-container {
            height: 120px;
            display: flex;
            align-items: flex-end;
            gap: 4px;
            margin-top: 15px;
        }

        .graph-bar {
            flex: 1;
            background: #dfe6e9;
            border-radius: 3px;
            position: relative;
            transition: all 0.3s ease;
        }

        .graph-bar:hover {
            background: var(--accent);
            transform: scaleY(1.05);
        }

        .graph-bar.active {
            background: var(--accent);
        }

        .months {
            display: flex;
            justify-content: space-between;
            margin-top: 10px;
            color: var(--secondary);
            font-size: 0.85rem;
        }

        .activity-list {
            list-style: none;
        }

        .activity-list li {
            margin-bottom: 15px;
            padding-left: 25px;
            position: relative;
        }

        .activity-list li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--accent);
            font-weight: bold;
        }

        .emoji {
            font-size: 1.2rem;
            margin-right: 5px;
            opacity: 0.9;
        }

        .footer {
            text-align: center;
            padding: 25px;
            color: var(--secondary);
            font-size: 0.9rem;
            border-top: 1px solid #eee;
            margin-top: 30px;
        }

        @media (max-width: 768px) {
            .header {
                padding: 30px 20px;
            }
            
            .name {
                font-size: 2.2rem;
            }
            
            .content-grid {
                grid-template-columns: 1fr;
            }
            
            .info-item {
                flex-direction: column;
                gap: 5px;
            }
            
            .info-label {
                min-width: auto;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header -->
        <header class="header">
            <h1 class="name">VULIANYS BANQUEZ</h1>
            <span class="username"><span class="emoji">👩‍💻</span> Vulli-dévy</span>
            <p class="tagline">Estudiante de Análisis y Desarrollo de Software <span class="emoji">🎓</span> | Apasionada por el desarrollo web <span class="emoji">💻</span> | Construyendo proyectos con <span class="highlight">HTML</span>, <span class="highlight">CSS</span> y <span class="highlight">JavaScript</span> mientras aprendo cada día <span class="emoji">📈</span></p>
            
            <div class="tech-icons">
                <i class="fab fa-html5" title="HTML5"></i>
                <i class="fab fa-css3-alt" title="CSS3"></i>
                <i class="fab fa-js" title="JavaScript"></i>
                <i class="fab fa-git-alt" title="Git"></i>
                <i class="fab fa-github" title="GitHub"></i>
            </div>
            
            <a href="#profile" class="link" style="font-weight: 600;"><span class="emoji">⚙️</span> Editar perfil</a>
        </header>

        <!-- Main Content -->
        <div class="content-grid">
            <!-- Profile Card -->
            <div class="card" id="profile">
                <h2 class="card-title"><i class="fas fa-user-circle"></i> Información del perfil</h2>
                
                <div class="info-item">
                    <span class="info-label"><span class="emoji">📅</span> Año regulatorio:</span>
                    <span class="info-value">1 siguiente</span>
                </div>
                
                <div class="info-item">
                    <span class="info-label"><span class="emoji">🏢</span> Organización:</span>
                    <span class="info-value">Management/Organizacion</span>
                </div>
                
                <div class="info-item">
                    <span class="info-label"><span class="emoji">🔗</span> Enlace:</span>
                    <span class="info-value">
                        <a href="https://www.banquuez.com/fayalang/~banquez-nuevo-adaptacion/es-mensabans-banquetada/lapalanga_perfile_view_base_const_d_definitiv_basnoboyjmbio.umitivo/svx0s_cpa2v3v2b" class="link" target="_blank">
                            Ver perfil completo
                        </a>
                    </span>
                </div>
            </div>

            <!-- Contributions Card -->
            <div class="card">
                <h2 class="card-title"><i class="fas fa-chart-line"></i> Contribuciones</h2>
                
                <div class="info-item">
                    <span class="info-label"><span class="emoji">📊</span> Último año:</span>
                    <span class="info-value">16 contribuciones</span>
                </div>
                
                <div class="contribution-graph">
                    <p><strong><span class="emoji">🗓️</span> Actividad anual:</strong></p>
                    <div class="graph-container" id="graph">
                        <!-- Graph bars will be generated by JavaScript -->
                    </div>
                    <div class="months">
                        <span>Ene</span>
                        <span>Feb</span>
                        <span>Mar</span>
                        <span>Abr</span>
                        <span>May</span>
                        <span>Jun</span>
                        <span>Jul</span>
                        <span>Ago</span>
                        <span>Sep</span>
                        <span>Oct</span>
                        <span>Nov</span>
                        <span>Dic</span>
                    </div>
                </div>
                
                <p style="margin-top: 20px; font-size: 0.9rem; color: var(--secondary);">
                    <span class="emoji">💡</span> Cómo se calculan las contribuciones
                </p>
            </div>

            <!-- Recent Activity Card -->
            <div class="card">
                <h2 class="card-title"><i class="fas fa-history"></i> Actividad reciente</h2>
                <p style="margin-bottom: 15px; color: var(--secondary);"><strong><span class="emoji">📅</span> Diciembre 2023</strong></p>
                
                <ul class="activity-list">
                    <li>Creado 3 commits en 1 repositorio</li>
                    <li>Villi-dévy/tulli-dévy 3 semejantes</li>
                    <li>Creó su primer repositorio</li>
                    <li>12 de diciembre</li>
                </ul>
            </div>

            <!-- Goals Card -->
            <div class="card">
                <h2 class="card-title"><i class="fas fa-bullseye"></i> Objetivos 2024</h2>
                
                <ul class="activity-list">
                    <li>Completar 100 contribuciones en GitHub</li>
                    <li>Desarrollar 5 proyectos web completos</li>
                    <li>Aprender un framework frontend (React/Vue)</li>
                    <li>Contribuir a un proyecto open-source</li>
                    <li>Mejorar habilidades en Git y control de versiones</li>
                </ul>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p><span class="emoji">✨</span> Siempre aprendiendo, siempre creciendo <span class="emoji">🚀</span></p>
            <p style="margin-top: 10px;">Última actualización: Diciembre 2023</p>
        </div>
    </div>

    <script>
        // Generate contribution graph
        document.addEventListener('DOMContentLoaded', function() {
            const graphContainer = document.getElementById('graph');
            const contributions = [2, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 5]; // Sample data
            
            // Normalize data for graph
            const maxContributions = Math.max(...contributions);
            
            contributions.forEach((count, index) => {
                const bar = document.createElement('div');
                bar.className = 'graph-bar';
                
                // Make the last bar (December) active
                if (index === contributions.length - 1) {
                    bar.classList.add('active');
                }
                
                // Calculate height based on contributions
                const height = maxContributions > 0 ? (count / maxContributions) * 100 : 10;
                bar.style.height = `${height}%`;
                
                // Add tooltip
                bar.title = `${count} contribuciones`;
                
                graphContainer.appendChild(bar);
            });
            
            // Add animation to bars on hover
            const bars = document.querySelectorAll('.graph-bar');
            bars.forEach(bar => {
                bar.addEventListener('mouseenter', function() {
                    this.style.transform = 'scaleY(1.1)';
                });
                
                bar.addEventListener('mouseleave', function() {
                    if (!this.classList.contains('active')) {
                        this.style.transform = 'scaleY(1)';
                    }
                });
            });
        });
    </script>
</body>
</html>

