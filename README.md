<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Thomas Sexton | Senior Systems Engineer</title>
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">

    <style>
        :root {
            /* Engineering Color Palette */
            --bg-dark: #121212;
            --bg-card: #1e1e1e;
            --accent-blue: #3b82f6; /* Schematic Blue */
            --accent-volt: #facc15; /* High Voltage Yellow */
            --text-main: #e5e5e5;
            --text-muted: #a3a3a3;
            --border-color: #333;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-main);
            line-height: 1.6;
        }

        /* --- Technical Background Pattern (PCB Trace Effect) --- */
        .bg-pattern {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background-color: var(--bg-dark);
            background-image: 
                radial-gradient(var(--border-color) 1px, transparent 1px), 
                radial-gradient(var(--border-color) 1px, transparent 1px);
            background-size: 20px 20px;
            background-position: 0 0, 10px 10px;
            opacity: 0.2;
        }

        h1, h2, h3, .mono-font {
            font-family: 'Space Mono', monospace;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* --- Header / Hero --- */
        header {
            padding: 80px 0;
            border-bottom: 1px solid var(--border-color);
        }

        .hero-title {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .hero-subtitle {
            color: var(--accent-blue);
            font-size: 1.2rem;
            margin-bottom: 20px;
        }

        .hero-bio {
            max-width: 600px;
            color: var(--text-muted);
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            padding: 10px 20px;
            border: 2px solid var(--accent-blue);
            color: var(--accent-blue);
            text-decoration: none;
            font-family: 'Space Mono', monospace;
            font-weight: bold;
            transition: 0.3s;
            border-radius: 4px;
        }

        .btn:hover {
            background: var(--accent-blue);
            color: white;
        }

        /* --- Skills Section --- */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }

        .skill-card {
            background: var(--bg-card);
            padding: 20px;
            border-left: 3px solid var(--accent-volt);
            border-radius: 4px;
        }

        .skill-card i {
            color: var(--accent-volt);
            margin-bottom: 10px;
            font-size: 1.5rem;
        }

        /* --- Portfolio / Case Studies --- */
        .section-title {
            font-size: 1.8rem;
            margin: 60px 0 30px 0;
            border-bottom: 2px solid var(--border-color);
            padding-bottom: 10px;
            display: inline-block;
        }

        .project-card {
            background: var(--bg-card);
            border: 1px solid var(--border-color);
            margin-bottom: 30px;
            border-radius: 8px;
            overflow: hidden;
            transition: transform 0.2s;
        }

        .project-card:hover {
            transform: translateY(-5px);
            border-color: var(--accent-blue);
        }

        .project-header {
            padding: 20px;
            background: rgba(59, 130, 246, 0.1);
            border-bottom: 1px solid var(--border-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .project-body {
            padding: 25px;
        }

        .tag {
            background: #333;
            color: #fff;
            padding: 4px 8px;
            font-size: 0.8rem;
            border-radius: 4px;
            margin-right: 5px;
            font-family: 'Space Mono', monospace;
        }

        /* --- Footer --- */
        footer {
            text-align: center;
            padding: 40px 0;
            color: var(--text-muted);
            font-size: 0.9rem;
            margin-top: 60px;
            border-top: 1px solid var(--border-color);
        }
        
        /* Mobile Tweaks */
        @media (max-width: 600px) {
            .hero-title { font-size: 2rem; }
            .project-header { flex-direction: column; align-items: flex-start; gap: 10px; }
        }
    </style>
</head>
<body>

    <div class="bg-pattern"></div>

    <div class="container">
        
        <header>
            <h1 class="hero-title">Thomas Sexton<span style="color:var(--accent-volt)">.</span>xyz</h1>
            <h3 class="hero-subtitle mono-font">> Senior Systems Engineer | Hardware & Firmware Integration</h3>
            
            <p class="hero-bio">
                Specializing in <strong>High Voltage (750V+)</strong> systems, <strong>Embedded Autonomy</strong>, and ruggedized hardware for harsh environments (Rail, Naval, & Automotive). 
                I bridge the gap between mechanical constraints and low-level firmware.
            </p>

            <a href="mailto:your-email@example.com" class="btn">
                <i class="fas fa-envelope"></i> Contact for Contracting
            </a>
            <a href="#" class="btn" style="margin-left: 10px; border-color: #555; color: #aaa;">
                <i class="fas fa-file-alt"></i> View Resume
            </a>
        </header>

        <section>
            <div class="skills-grid">
                <div class="skill-card">
                    <i class="fas fa-bolt"></i>
                    <h4>High Voltage Systems</h4>
                    <p class="mono-font" style="font-size: 0.9rem; color: #bbb;">750V-1000V DC power distribution, isolation safety, & arc flash prevention.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-microchip"></i>
                    <h4>Embedded Firmware</h4>
                    <p class="mono-font" style="font-size: 0.9rem; color: #bbb;">C/C++ for STM32 & Real-Time systems. Lidar/Sensor integration.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-car-battery"></i>
                    <h4>Automotive / CAN Bus</h4>
                    <p class="mono-font" style="font-size: 0.9rem; color: #bbb;">Custom harness design, ECU communication, & reverse engineering.</p>
                </div>
                <div class="skill-card">
                    <i class="fas fa-print"></i>
                    <h4>Rapid Prototyping</h4>
                    <p class="mono-font" style="font-size: 0.9rem; color: #bbb;">3D Scanning/Printing for mechanical fitment & custom enclosures.</p>
                </div>
            </div>
        </section>

        <section>
            <h2 class="section-title">Selected Case Studies</h2>

            <div class="project-card">
                <div class="project-header">
                    <h3>High-Voltage EV Control for Rail</h3>
                    <span class="mono-font" style="color:var(--accent-volt)">[Industrial]</span>
                </div>
                <div class="project-body">
                    <p><strong>The Challenge:</strong> Designing safe, reliable control systems for 750V-1000V DC electric rail vehicles.</p>
                    <br>
                    <p><strong>The Solution:</strong> Developed full electrical harness layouts and control software, ensuring isolation compliance and redundant safety interlocks. Integrated diesel/electric hybrid control strategies.</p>
                    <br>
                    <div>
                        <span class="tag">High Voltage</span>
                        <span class="tag">System Architecture</span>
                        <span class="tag">SolidWorks Electrical</span>
                    </div>
                </div>
            </div>

            <div class="project-card">
                <div class="project-header">
                    <h3>LIDAR & Autonomy Integration</h3>
                    <span class="mono-font" style="color:var(--accent-blue)">[Defense / Naval]</span>
                </div>
                <div class="project-body">
                    <p><strong>The Challenge:</strong> Retrofitting autonomy onto existing US Naval vessels for harsh saltwater environments.</p>
                    <br>
                    <p><strong>The Solution:</strong> Designed custom PCBs and low-level firmware to interface Lidar sensors with the vessel's navigation stack. Solved vibration and corrosion challenges inherent to ocean-going hardware.</p>
                    <br>
                    <div>
                        <span class="tag">Lidar</span>
                        <span class="tag">Embedded C</span>
                        <span class="tag">PCB Design</span>
                    </div>
                </div>
            </div>

            <div class="project-card">
                <div class="project-header">
                    <h3>Restomod Engineering: MR2 to Pulsar Swap</h3>
                    <span class="mono-font" style="color:#22c55e">[Automotive / Personal]</span>
                </div>
                <div class="project-body">
                    <p><strong>The Challenge:</strong> Integrating a 1991 Toyota powertrain into a 1987 Nissan chassis with zero OEM support.</p>
                    <br>
                    <p><strong>The
