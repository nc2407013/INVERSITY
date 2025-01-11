<!DOCTYPE html>
<html lang="en" class="govuk-template">
<head>
    <meta charset="utf-8">
    <title>Get help with GOV.UK - Hermes AI Assistant - GOV.UK</title>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/govuk-frontend/4.7.0/govuk-frontend.min.css">
    <style>
        .ai-container {
            background: #f3f2f1;
            padding: 20px;
            border: 1px solid #b1b4b6;
            margin: 30px 0;
        }
        .chat-area {
            background: white;
            padding: 15px;
            border: 2px solid #b1b4b6;
            height: 400px;
            margin-bottom: 20px;
            overflow-y: auto;
        }
        .search-container {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }
        .ai-message {
            background: #f3f2f1;
            padding: 15px;
            border-radius: 4px;
            margin-bottom: 10px;
            max-width: 80%;
        }
        .user-message {
            background: #1d70b8;
            color: white;
            padding: 15px;
            border-radius: 4px;
            margin-bottom: 10px;
            margin-left: auto;
            max-width: 80%;
        }
        .thinking {
            display: none;
            color: #505a5f;
            font-style: italic;
            margin: 10px 0;
        }
        .related-links {
            background: #ffffff;
            padding: 15px;
            margin-top: 10px;
            border-top: 2px solid #1d70b8;
        }
        .feedback-buttons {
            display: flex;
            gap: 10px;
            margin-top: 5px;
        }
        .breadcrumbs {
            padding: 15px 0;
            border-bottom: 1px solid #b1b4b6;
            margin-bottom: 20px;
        }
    </style>
</head>
<body class="govuk-template__body">
    <a href="#main-content" class="govuk-skip-link" data-module="govuk-skip-link">Skip to main content</a>

    <header class="govuk-header" role="banner" data-module="govuk-header">
        <div class="govuk-header__container govuk-width-container">
            <div class="govuk-header__logo">
                <a href="https://www.gov.uk" class="govuk-header__link govuk-header__link--homepage">
                    <span class="govuk-header__logotype">
                        GOV.UK
                    </span>
                </a>
            </div>
            <div class="govuk-header__content">
                <a href="/hermes" class="govuk-header__link govuk-header__service-name">
                    Hermes AI Assistant
                </a>
                <nav aria-label="Menu" class="govuk-header__navigation">
                    <button type="button" class="govuk-header__menu-button govuk-js-header-toggle" aria-controls="navigation" aria-label="Show or hide menu">Menu</button>
                    <ul id="navigation" class="govuk-header__navigation-list">
                        <li class="govuk-header__navigation-item govuk-header__navigation-item--active">
                            <a class="govuk-header__link" href="#" aria-current="page">
                                Home
                            </a>
                        </li>
                        <li class="govuk-header__navigation-item">
                            <a class="govuk-header__link" href="#">
                                Help guides
                            </a>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <div class="govuk-width-container">
        <div class="breadcrumbs">
            <div class="govuk-breadcrumbs">
                <ol class="govuk-breadcrumbs__list">
                    <li class="govuk-breadcrumbs__list-item">
                        <a class="govuk-breadcrumbs__link" href="https://www.gov.uk">Home</a>
                    </li>
                    <li class="govuk-breadcrumbs__list-item">
                        <a class="govuk-breadcrumbs__link">Hermes AI Assistant</a>
                    </li>
                </ol>
            </div>
        </div>

        <main class="govuk-main-wrapper" id="main-content" role="main">
            <h1 class="govuk-heading-xl">Get help with GOV.UK services</h1>
            
            <div class="govuk-grid-row">
                <div class="govuk-grid-column-two-thirds">
                    <div class="govuk-notification-banner govuk-notification-banner--success" role="alert">
                        <div class="govuk-notification-banner__header">
                            <h2 class="govuk-notification-banner__title">Beta Service</h2>
                        </div>
                        <div class="govuk-notification-banner__content">
                            <p class="govuk-notification-banner__heading">
                                Hermes is a new service to help you find information more easily
                            </p>
                        </div>
                    </div>
                    
                    <div class="ai-container">
                        <div class="chat-area" id="chatArea">
                            <div class="ai-message">
                                Hello, I'm Hermes, your GOV.UK assistant. I can help you:
                                <ul class="govuk-list govuk-list--bullet">
                                    <li>Find specific government services</li>
                                    <li>Understand application processes</li>
                                    <li>Navigate to the right forms and guidance</li>
                                    <li>Answer questions about government services</li>
                                </ul>
                                How can I help you today?
                            </div>
                        </div>
                        
                        <div class="thinking" id="thinking">Hermes is thinking...</div>
                        
                        <div class="search-container">
                            <input type="text" class="govuk-input" id="searchInput" placeholder="Type your question here..." aria-label="Search input">
                            <button class="govuk-button" data-module="govuk-button" onclick="sendMessage()">
                                Ask Hermes
                            </button>
                        </div>
                    </div>

                    <div class="govuk-inset-text">
                        Your conversation with Hermes is not stored and will be cleared when you close this page.
                    </div>
                </div>

                <div class="govuk-grid-column-one-third">
                    <aside class="govuk-related-items">
                        <h2 class="govuk-heading-m">Popular services</h2>
                        <ul class="govuk-list">
                            <li><a class="govuk-link" href="https://www.gov.uk/browse/benefits">Benefits</a></li>
                            <li><a class="govuk-link" href="https://www.gov.uk/browse/driving">Driving and transport</a></li>
                            <li><a class="govuk-link" href="https://www.gov.uk/browse/working">Working, jobs and pensions</a></li>
                            <li><a class="govuk-link" href="https://www.gov.uk/browse/tax">Money and tax</a></li>
                        </ul>
                    </aside>
                </div>
            </div>
        </main>
    </div>

    <footer class="govuk-footer" role="contentinfo">
        <div class="govuk-width-container">
            <div class="govuk-footer__meta">
                <div class="govuk-footer__meta-item govuk-footer__meta-item--grow">
                    <h2 class="govuk-visually-hidden">Support links</h2>
                    <ul class="govuk-footer__inline-list">
                        <li class="govuk-footer__inline-list-item">
                            <a class="govuk-footer__link" href="#">Accessibility</a>
                        </li>
                        <li class="govuk-footer__inline-list-item">
                            <a class="govuk-footer__link" href="#">Cookies</a>
                        </li>
                        <li class="govuk-footer__inline-list-item">
                            <a class="govuk-footer__link" href="#">Privacy</a>
                        </li>
                        <li class="govuk-footer__inline-list-item">
                            <a class="govuk-footer__link" href="#">Terms and conditions</a>
                        </li>
                    </ul>
                    <div class="govuk-footer__meta-custom">
                        Built by the Government Digital Service
                    </div>
                </div>
                <div class="govuk-footer__meta-item">
                    <a class="govuk-footer__link govuk-footer__copyright-logo" href="https://www.nationalarchives.gov.uk/information-management/re-using-public-sector-information/uk-government-licensing-framework/crown-copyright/">© Crown copyright</a>
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Initialize chat functionality
        const chatArea = document.getElementById('chatArea');
        const searchInput = document.getElementById('searchInput');
        const thinking = document.getElementById('thinking');

        // Knowledge base for Hermes (this would be much more extensive in production)
        const knowledgeBase = {
            'passport': {
                response: "To apply for or renew a passport, you can use the online service at GOV.UK. The current fee is £75.50 for online applications. Processing usually takes around 3 weeks.",
                links: [
                    { text: "Apply for a passport", url: "https://www.gov.uk/apply-renew-passport" },
                    { text: "Check processing times", url: "https://www.gov.uk/guidance/passport-processing-times" }
                ]
            },
            'universal credit': {
                response: "Universal Credit is a payment to help with living costs. You may be eligible if you're on a low income, out of work, or cannot work.",
                links: [
                    { text: "Apply for Universal Credit", url: "https://www.gov.uk/universal-credit" },
                    { text: "Check if you're eligible", url: "https://www.gov.uk/universal-credit/eligibility" }
                ]
            },
            'council tax': {
                response: "Council Tax is a tax on domestic properties collected by your local council. The amount you pay depends on your property's band and where you live.",
                links: [
                    { text: "Check your Council Tax band", url: "https://www.gov.uk/council-tax-bands" },
                    { text: "Apply for Council Tax Reduction", url: "https://www.gov.uk/apply-council-tax-reduction" }
                ]
            }
        };

        // Function to add a message to the chat
        function addMessage(message, isUser = false) {
            const messageDiv = document.createElement('div');
            messageDiv.className = isUser ? 'user-message' : 'ai-message';
            messageDiv.innerHTML = message;
            chatArea.appendChild(messageDiv);
            chatArea.scrollTop = chatArea.scrollHeight;
        }

        // Function to handle user input
        function sendMessage() {
            const userInput = searchInput.value.trim().toLowerCase();
            if (!userInput) return;

            // Add user message
            addMessage(searchInput.value, true);
            searchInput.value = '';

            // Show thinking indicator
            thinking.style.display = 'block';

            // Simulate AI processing (would be replaced with actual API call)
            setTimeout(() => {
                thinking.style.display = 'none';
                
                // Search knowledge base for relevant response
                let foundResponse = false;
                for (const [key, data] of Object.entries(knowledgeBase)) {
                    if (userInput.includes(key)) {
                        let response = data.response;
                        if (data.links) {
                            response += '<div class="related-links"><h3 class="govuk-heading-s">Relevant links:</h3><ul class="govuk-list govuk-list--bullet">';
                            data.links.forEach(link => {
                                response += `<li><a href="${link.url}" class="govuk-link">${link.text}</a></li>`;
                            });
                            response += '</ul></div>';
                        }
                        addMessage(response);
                        foundResponse = true;
                        break;
                    }
                }

                if (!foundResponse) {
                    addMessage("I apologize, but I couldn't find specific information about that. You might find what you're looking for in these sections:<br><br>" +
                        '<ul class="govuk-list govuk-list--bullet">' +
                        '<li><a href="https://www.gov.uk/browse/benefits" class="govuk-link">Benefits</a></li>' +
                        '<li><a href="https://www.gov.uk/browse/working" class="govuk-link">Working, jobs and pensions</a></li>' +
                        '<li><a href="https://www.gov.uk/browse/tax" class="govuk-link">Money and tax</a></li>' +
                        '</ul>');
                }
            }, 1000);
        }

        // Handle Enter key in input
        searchInput.addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                sendMessage();
            }
        });
    </script>
</body>
</html>
