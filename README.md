
    <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Goal Gappa - Your Study Partner</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700&family=Oswald:wght@700&display=swap" rel="stylesheet">

    <!-- 
      This <style> block contains all the "old-fashioned" CSS.
      This is the equivalent of a separate .css file.
    -->

    <style>
        /* --- Global Resets & Font Definitions --- */

        
        :root {
            --brand-red: #FF4B2B;
            --brand-orange: #FF785A;
            --brand-bg: #121212;
            --brand-card: #1E1E1E;
            --brand-border: #2a2a2a;
            --text-primary: #E5E7EB; /* gray-200 */
            --text-secondary: #D1D5DB; /* gray-300 */
            --text-muted: #6B7280; /* gray-500 */
        }

        * {
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            margin: 0;
            background-color: var(--brand-bg);
            color: var(--text-primary);
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        h1, h2, h3 {
            font-family: 'Oswald', sans-serif;
            text-transform: uppercase;
            color: #FFFFFF;
            margin-top: 0;
        }

        h1 {
            font-size: 3rem; /* 48px */
            font-weight: 700;
            color: var(--brand-red);
        }

        h2 {
            font-size: 1.875rem; /* 30px */
            font-weight: 700;
            margin-bottom: 2rem;
            text-align: center;
        }

        h3 {
            font-size: 1.5rem; /* 24px */
            font-weight: 700;
            color: var(--brand-red);
            margin-bottom: 1rem;
        }

        /* --- Utility Class --- */
        .hidden {
            display: none;
        }
        
        /* --- Layout --- */
        .section-container {
            width: 100%;
            max-width: 1152px; /* 72rem */
            margin-left: auto;
            margin-right: auto;
            padding: 4rem 1.5rem; /* py-16 px-6 */
        }
        
        /* --- Header & Navigation --- */
        .header {
            position: sticky;
            top: 0;
            z-index: 50;
            width: 100%;
            background-color: rgba(18, 18, 18, 0.9);
            backdrop-filter: blur(4px);
            border-bottom: 1px solid var(--brand-border);
        }
        
        .navbar {
            max-width: 1152px;
            margin-left: auto;
            margin-right: auto;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 1rem;
        }
        
        .logo {
            font-size: 1.5rem; /* 24px */
            font-family: 'Oswald', sans-serif;
            font-weight: 700;
            color: var(--brand-red);
            text-decoration: none;
        }
        
        .nav-links {
            display: none; /* Hidden on mobile */
            align-items: center;
            gap: 0.5rem;
        }
        
        .nav-link {
            padding: 0.5rem 1rem;
            border-radius: 0.375rem; /* 6px */
            font-size: 0.875rem; /* 14px */
            font-weight: 500;
            color: var(--text-secondary);
            text-decoration: none;
            transition: color 0.3s ease, background-color 0.3s ease;
        }

        .nav-link:hover {
            background-color: var(--brand-red);
            color: #FFFFFF;
        }

        #mobile-menu-btn {
            display: block; /* Show on mobile */
            padding: 0.5rem;
            border-radius: 0.375rem;
            color: var(--text-secondary);
            background: none;
            border: none;
            cursor: pointer;
        }
        
        #mobile-menu-btn:hover {
            background-color: var(--brand-red);
            color: #FFFFFF;
        }
        
        #mobile-menu-btn svg {
            width: 1.5rem;
            height: 1.5rem;
        }

        #mobile-menu {
            border-top: 1px solid var(--brand-border);
        }

        #mobile-menu .nav-link {
            display: block;
            text-align: center;
        }
        
        /* --- Components --- */
        .card {
            background-color: var(--brand-card);
            padding: 1.5rem;
            border-radius: 0.75rem; /* 12px */
            border: 1px solid var(--brand-border);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
        
        .btn {
            background-color: var(--brand-red);
            color: #FFFFFF;
            font-family: 'Oswald', sans-serif;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            font-weight: 700;
            padding: 0.75rem 1.5rem;
            border-radius: 0.5rem; /* 8px */
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
        }
        
        .btn:hover {
            background-color: var(--brand-orange);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            transform: translateY(-2px);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--brand-red);
            color: var(--brand-red);
            font-family: 'Oswald', sans-serif;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            font-weight: 700;
            padding: 0.75rem 1.5rem;
            border-radius: 0.5rem;
            transition: all 0.3s ease;
            cursor: pointer;
        }
        
        .btn-outline:hover {
            background-color: var(--brand-red);
            color: #FFFFFF;
        }
        
        .form-input {
            width: 100%;
            background-color: var(--brand-bg);
            border: 1px solid var(--brand-border);
            color: var(--text-primary);
            border-radius: 0.5rem;
            padding: 0.75rem 1rem;
            font-size: 1rem;
        }
        
        .form-input::placeholder {
            color: var(--text-muted);
        }
        
        .form-input:focus {
            outline: none;
            border-color: var(--brand-red);
            box-shadow: 0 0 0 2px var(--brand-red);
        }

        /* --- Page Sections --- */
        #hero {
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
        }

        #hero p {
            font-size: 1.25rem; /* 20px */
            color: var(--text-secondary);
            max-width: 672px; /* 42rem */
            margin-bottom: 2rem;
        }

        #goal-setter {
            background-color: var(--brand-card);
            border-top-left-radius: 1.5rem;
            border-top-right-radius: 1.5rem;
        }

        .goal-setter-content {
            max-width: 896px; /* 56rem */
            margin-left: auto;
            margin-right: auto;
        }
        
        #task-form {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-bottom: 2rem;
        }
        
        #task-input {
            flex-grow: 1;
        }
        
        .task-list-container {
            margin-bottom: 2rem;
        }
        
        .task-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
            background-color: var(--brand-bg);
            padding: 1rem;
            border-radius: 0.5rem;
            border: 1px solid var(--brand-border);
            margin-bottom: 0.75rem;
        }
        
        .task-item span {
            flex-grow: 1;
            padding-right: 1rem;
            word-break: break-word;
        }

        .task-item.completed span {
            text-decoration: line-through;
            color: var(--text-muted);
        }
        
        .task-item .task-buttons {
            flex-shrink: 0;
        }
        
        .task-item button {
            background: none;
            border: none;
            cursor: pointer;
        }

        .complete-btn {
            color: #22C55E; /* green-500 */
            margin-right: 0.75rem;
        }
        .complete-btn:hover { color: #4ADE80; } /* green-400 */

        .delete-btn {
            color: #EF4444; /* red-500 */
        }
        .delete-btn:hover { color: #F87171; } /* red-400 */

        .complete-btn svg,
        .delete-btn svg {
            width: 1.5rem;
            height: 1.5rem;
        }

        #no-tasks {
            text-align: center;
            color: var(--text-muted);
        }

        .checkin-card {
            max-width: 896px;
            margin-left: auto;
            margin-right: auto;
            text-align: center;
        }
        
        #checkin-buttons {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 1.5rem;
        }
        
        #checkin-buttons .btn-outline {
            width: 10rem;
        }
        
        #checkin-message {
            font-size: 1.125rem; /* 18px */
            color: var(--brand-orange);
            font-weight: 500;
            height: 1.5rem; /* for layout stability */
        }
        
        #features {
            background-color: var(--brand-card);
            border-bottom-left-radius: 1.5rem;
            border-bottom-right-radius: 1.5rem;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1.5rem;
        }
        
        .features-grid .card {
            background-color: var(--brand-bg);
        }

        .features-grid p {
            color: var(--text-secondary);
            margin: 0;
        }

        .footer {
            text-align: center;
            padding-top: 4rem;
            padding-bottom: 4rem;
            border-top: 1px solid var(--brand-border);
        }
        
        .footer h4 {
            font-size: 1.5rem;
            font-family: 'Oswald', sans-serif;
            font-weight: 700;
            color: var(--brand-red);
            margin: 0 0 1rem 0;
        }
        
        .footer p {
            color: var(--text-muted);
            margin: 0;
        }

        /* --- Responsive Media Queries --- */
        @media (min-width: 768px) { /* md breakpoint */
            h1 {
                font-size: 6rem; /* 96px */
            }
            h2 {
                font-size: 3rem; /* 48px */
            }
            .section-container {
                padding-top: 6rem;
                padding-bottom: 6rem;
            }
            .nav-links {
                display: flex;
            }
            #mobile-menu-btn {
                display: none;
            }
            #mobile-menu {
                display: none !important; /* Ensure it's hidden on desktop */
            }
            #hero p {
                font-size: 1.5rem; /* 24px */
            }
            #task-form {
                flex-direction: row;
            }
            .features-grid {
                grid-template-columns: repeat(3, 1fr);
            }
        }

    </style>
</head>
<body>

    <!-- Header & Navigation -->
    <header class="header">
        <nav class="navbar">
            <a href="#hero" class="logo">GOAL GAPPA</a>
            <div class="nav-links">
                <a href="#goal-setter" class="nav-link">Goal Setter</a>
                <a href="#check-in" class="nav-link">Check-In</a>
                <a href="#features" class="nav-link">Features</a>
            </div>
            <button id="mobile-menu-btn">
                <!-- Mobile Menu Icon (Hamburger) -->
                <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-8 6h8"></path></svg>
            </button>
        </nav>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden">
            <a href="#goal-setter" class="nav-link mobile-nav-link">Goal Setter</a>
            <a href="#check-in" class="nav-link mobile-nav-link">Check-In</a>
            <a href="#features" class="nav-link mobile-nav-link">Features</a>
        </div>
    </header>

    <!-- Main Content -->
    <main>

        <!-- Hero Section -->
        <section id="hero" class="section-container">
            <h1>GOAL GAPPA</h1>
            <p>
                Stop procrastinating. Start achieving.
                <br>
                Gamify your studies and hit your targets.
            </p>
            <a href="#goal-setter" class="btn">Set Your First Goal</a>
        </section>

        <!-- Goal Setter Section (Interactive) -->
        <section id="goal-setter" class="section-container">
            <div class="goal-setter-content">
                <h2>Your Goal Setter</h2>
                <div class="card">
                    <form id="task-form">
                        <input type="text" id="task-input" class="form-input" placeholder="e.g., 'Finish Chapter 3 reading'">
                        <button type="submit" class="btn">Add Goal</button>
                    </form>
                </div>
                
                <!-- Task List -->
                <div class="card task-list-container">
                    <h3>Active Goals</h3>
                    <div id="task-list">
                        <!-- Tasks will be injected here by JS -->
                    </div>
                    <p id="no-tasks">You have no active goals. Add one above!</p>
                </div>
            </div>
        </section>

        <!-- Mental Health Check-in Section (Interactive) -->
        <section id="check-in" class="section-container">
            <div class="card checkin-card">
                <h2>Mental Health Check-In</h2>
                <h3>How are you feeling today?</h3>
                <p style="color: var(--text-secondary); margin-bottom: 2rem;">A quick check-in helps us support you better.</p>
                
                <div id="checkin-buttons">
                    <button class="btn-outline" onclick="handleCheckin('Great')">Great! 😄</button>
                    <button class="btn-outline" onclick="handleCheckin('Okay')">Just Okay 😐</button>
                    <button class="btn-outline" onclick="handleCheckin('Stressed')">Stressed 😫</button>
                    <button class="btn-outline" onclick="handleCheckin('Overwhelmed')">Overwhelmed 😥</button>
                </div>
                
                <div id="checkin-message">
                    <!-- Message appears here -->
                </div>
            </div>
        </section>

        <!-- Other Features Section (Static) -->
        <section id="features" class="section-container">
            <h2>Core Features</h2>
            <div class="features-grid">
                <div class="card">
                    <h3>Scoreboards</h3>
                    <p>See how you stack up against friends. Friendly competition to keep you motivated.</p>
                </div>
                <div class="card">
                    <h3>Reward System</h3>
                    <p>Complete goals to earn points. Unlock badges and achievements for your hard work.</p>
                </div>
                <div class="card">
                    <h3>Game Central</h3>
                    <p>Take a break with quick, fun brain games designed to sharpen your mind.</p>
                </div>
            </div>
        </section>

    </main>

    <!-- Footer -->
    <footer class="footer">
        <h4>GOAL GAPPA</h4>
        <p>From Team Bazigar | 2025</p>
    </footer>

    <!-- JavaScript for Interactivity -->
    <script>
        document.addEventListener('DOMContentLoaded', () => {

            // --- Mobile Menu ---
            const mobileMenuBtn = document.getElementById('mobile-menu-btn');
            const mobileMenu = document.getElementById('mobile-menu');
            mobileMenuBtn.addEventListener('click', () => {
                // Toggle the 'hidden' class to show/hide the menu
                mobileMenu.classList.toggle('hidden');
            });
            // Close mobile menu when a link is clicked
            document.querySelectorAll('.mobile-nav-link').forEach(link => {
                link.addEventListener('click', () => {
                    mobileMenu.classList.add('hidden');
                });
            });

            // --- Goal Setter ---
            const taskForm = document.getElementById('task-form');
            const taskInput = document.getElementById('task-input');
            const taskList = document.getElementById('task-list');
            const noTasksMsg = document.getElementById('no-tasks');

            taskForm.addEventListener('submit', (e) => {
                e.preventDefault();
                const taskText = taskInput.value.trim();
                
                if (taskText !== '') {
                    addTask(taskText);
                    taskInput.value = '';
                    updateNoTasksMessage();
                }
            });

            function addTask(text) {
                const taskItem = document.createElement('div');
                taskItem.className = 'task-item'; // Use the CSS class defined in <style>
                
                taskItem.innerHTML = `
                    <span>${text}</span>
                    <div class="task-buttons">
                        <button class="complete-btn" title="Complete">
                            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path></svg>
                        </button>
                        <button class="delete-btn" title="Delete">
                            <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"></path></svg>
                        </button>
                    </div>
                `;
                
                // Add event listeners for new buttons
                taskItem.querySelector('.complete-btn').addEventListener('click', () => {
                    taskItem.classList.toggle('completed');
                });
                
                taskItem.querySelector('.delete-btn').addEventListener('click', () => {
                    taskItem.remove();
                    updateNoTasksMessage();
                });
                
                taskList.appendChild(taskItem);
            }

            function updateNoTasksMessage() {
                // Use the 'hidden' class defined in <style>
                if (taskList.children.length === 0) {
                    noTasksMsg.classList.remove('hidden');
                } else {
                    noTasksMsg.classList.add('hidden');
                }
            }

            // Initial check
            updateNoTasksMessage();
        });

        // --- Mental Health Check-in ---
        function handleCheckin(feeling) {
            const messageEl = document.getElementById('checkin-message');
            let message = '';

            switch(feeling) {
                case 'Great':
                    message = "Awesome! Keep up the positive energy!";
                    break;
                case 'Okay':
                    message = "That's alright. A steady pace wins the race.";
                    break;
                case 'Stressed':
                    message = "Take a deep breath. Try a 5-min break.";
                    break;
                case 'Overwhelmed':
                    message = "It's okay to feel this way. Focus on one small task.";
                    break;
            }
            
            messageEl.textContent = message;

            // Hide the message after 3 seconds
            setTimeout(() => {
                messageEl.textContent = '';
            }, 3000);
        }

    </script>

</body>
</html>
