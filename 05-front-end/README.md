# AI-Assisted Front End Prototyping: Weather Data Dashboard

## Module Overview
This module demonstrates how GitHub Copilot can accelerate web development and prototyping for tech professionals in academic settings. Using a weather data dashboard as our example, we'll explore how AI coding assistants can help with everything from simple CSS reorganization to building modern, interactive features.

## Learning Objectives
- Master GitHub Copilot's core features (inline suggestions, chat, commands)
- Develop effective prompting strategies for AI-assisted coding
- Learn to manage context and file selection for optimal results
- Build confidence in using AI tools for rapid prototyping
- Understand when and how to iterate on AI suggestions

## The Scenario
We're working with a functional Flask-based weather data dashboard that needs modernization:
- A working Flask application displaying NOAA weather data
- Mixed concerns (CSS embedded in HTML)
- Basic functionality that could benefit from enhanced user experience
- Opportunities for both simple improvements and advanced features

## Project Structure
```
flask-app/
├── app.py                    # Flask application with data visualization
├── requirements.txt          # Python dependencies
├── Dockerfile               # Container configuration
├── docker-compose.yml       # Service orchestration
├── .env                     # Environment variables
├── static/
│   └── styles.css          # Currently minimal CSS file
├── templates/
│   ├── index.html          # Main page with embedded styles
│   └── layout.html         # Base template (unused)
└── README.md               # This file
```

## Module Flow

### Part 1: Getting Started with GitHub Copilot
Before diving into improvements, ensure you understand:
- **Inline Suggestions**: Tab to accept, Esc to dismiss
- **Copilot Chat**: Your AI pair programmer for discussions
- **Context Awareness**: How Copilot uses open files and project structure

### Part 2: Understanding Copilot Chat Modes

GitHub Copilot Chat offers three distinct modes, each designed for different development scenarios:

#### Ask Mode - Your Instant Code Assistant
**When to use**: Quick clarifications, code explanations, or learning without modifying files

**Key features**:
- No code changes are made
- Immediate context-aware help
- Perfect for understanding existing code

**Example exercises**:
1. Highlight the temperature plot generation code and ask: "How does this visualization work?"
2. Select the database connection code and ask: "What security improvements could be made here?"

#### Edit Mode - Surgical Code Updates
**When to use**: Specific, controlled changes to defined files

**Key features**:
- You choose which files can be modified
- Shows diffs before applying changes
- Full control over each edit

**Example exercises**:
1. Select multiple CSS rules and say: "Refactor these styles to use CSS custom properties"
2. Highlight a function and request: "Add error handling and logging to this function"

#### Agent Mode - Autonomous Development Partner
**When to use**: Complex, multi-step tasks requiring iteration

**Key features**:
- Autonomously determines files to modify
- Runs terminal commands (with approval)
- Iterates until task completion
- Self-corrects errors

**Example exercises**:
1. "Create a responsive navigation menu with home, statistics, and about pages"
2. "Implement a caching system for the weather data that refreshes every hour"
3. "Add comprehensive error handling across the entire application"

**Agent Mode Tips**:
- Use custom instructions to define coding standards
- Be specific about requirements
- Review the autonomous changes carefully
- Use the undo feature if needed

### Part 3: Enhanced Features

#### Web Search Integration (#web)
You can enhance any mode (Ask, Edit, or Agent) with web search capabilities by adding `#web` to your prompts:

**Examples**:
- "What are the latest Flask security best practices? #web"
- "How do I implement OAuth2 in Flask? #web"
- "Find modern CSS gradient examples for weather dashboards #web"

#### Screenshot Integration
Copilot Chat now supports image attachments for visual context:

**Use cases**:
1. **Design feedback**: Take a screenshot of your current UI, attach it, and ask: "Make this header more modern with a gradient background"
2. **Bug reports**: Screenshot an error and ask: "Why is this visualization not rendering correctly?"
3. **Mockup implementation**: Attach a design mockup and request: "Generate the HTML and CSS to match this design"

**Exercise**: 
1. Run your Flask app
2. Take a screenshot of the current temperature distribution chart
3. Attach it to Copilot Chat and ask: "Redesign this chart with a modern color scheme and better labels"

#### Model Selection
GitHub Copilot offers multiple AI models with different strengths:

**Available Models**:
- **Standard Models** (Included - no premium requests):
  - GPT-4.1 - Fast, general-purpose
  - GPT-4o - Optimized for code
  - GPT-5 mini (Preview) - Lightweight tasks

- **Premium Models** (Consume premium requests):
  - Claude Sonnet 3.5 (1x multiplier)
  - Claude Sonnet 3.7 (1x multiplier)  
  - Claude Sonnet 4 (1x multiplier) - **Recommended for complex tasks**
  - Gemini 2.5 Pro (1x multiplier)
  - GPT-5 (Preview) (1x multiplier)
  - o4-mini (Preview) (0.33x multiplier)

**Model Selection Tips**:
- Use standard models for routine coding tasks
- Switch to Claude 4 for complex refactoring or architectural decisions
- Experiment to find which model works best for your coding style

### Part 4: Basic Improvements - Learning the Fundamentals

#### 1. CSS Organization (Beginner)
**Goal**: Extract embedded CSS from `index.html` to `styles.css`

**Learning Points**:
- Using Copilot Chat's "Edit" mode
- Understanding file context selection
- Basic refactoring with AI assistance

**Exercise**:
1. Open both `index.html` and `styles.css` in your editor
2. Switch to Edit mode in Copilot Chat
3. Add both files to the context
4. Prompt: "Move all CSS from the style tag in index.html to styles.css while maintaining the same visual appearance"

#### 2. Theme Customization (Beginner)
**Goal**: Update fonts and color scheme

**Exercise Ideas**:
- Change to a modern font stack
- Update color palette to match university branding
- Adjust spacing and typography

**Prompting Strategy**:
```
"Update the color scheme to use [specific colors] for headers and 
[specific colors] for backgrounds. Change the font to [font name] 
and ensure good contrast for accessibility."
```

#### 3. Performance Optimization (Intermediate)
**Goal**: Cache the temperature distribution plot

**Using Agent Mode**:
1. Switch to Agent mode
2. Prompt: "Implement caching for the temperature distribution plot. Save it as a static image that regenerates every hour."
3. Watch as Copilot:
   - Analyzes the current implementation
   - Creates necessary directories
   - Implements caching logic
   - Adds cache invalidation

### Part 5: Intermediate Features - Building User Experience

#### 4. Dark Mode Implementation (Intermediate)
**Goal**: Add a toggle-able dark mode

**Progressive Approach with Edit Mode**:
1. Start: "Add a dark mode toggle button to the header"
2. Enhance: "Save the user's dark mode preference in localStorage"
3. Polish: "Add smooth transitions between light and dark modes"

**Screenshot Enhancement**:
- Take a screenshot after implementing basic dark mode
- Attach it and ask: "The dark mode looks too harsh. Make the colors more subtle with better contrast"

#### 5. Temperature Unit Converter (Intermediate)
**Goal**: Toggle between Celsius and Fahrenheit

**Demonstrating Prompting Excellence**:

**Basic Prompt**: 
"Add temperature converter"

**Better Prompt**: 
"Add a toggle button that converts all temperature displays between Celsius and Fahrenheit. Update the chart, statistics, and table data."

**Best Prompt with Context Questions**:
"I want to add a temperature unit converter to my weather dashboard. Before implementing, please ask me 3 questions about the specific requirements and user experience I'm looking for."

### Part 6: Advanced Features - Modern Web Development

#### 6. Multi-Page Navigation (Advanced)
**Goal**: Create a tabbed interface with multiple views

**Using Agent Mode**:
```
"Create a multi-page Flask application with:
- A navigation menu with Home, Statistics, Historical Trends, and About pages
- Use Flask blueprints for better organization
- Maintain consistent styling across all pages
- Add active page highlighting in the navigation"
```

#### 7. Modern UI Overhaul (Advanced)
**Goal**: Transform the dashboard into a contemporary web application

**Demonstrating Detailed Prompting**:

**Vague Prompt** (Don't do this):
"Make the site modern"

**Detailed Prompt** (Do this):
"Redesign the weather dashboard with a modern aesthetic:
- Use a card-based layout with subtle shadows (box-shadow: 0 2px 4px rgba(0,0,0,0.1))
- Implement a sticky navigation header with backdrop-filter blur
- Add hover animations (transform: translateY(-2px) on hover)
- Use a gradient color palette (#1a1a2e to #16213e)
- Ensure mobile responsiveness with CSS Grid
- Include skeleton loaders for data fetching states
- Add micro-interactions for all buttons and links"

## Prompting Best Practices

### 1. Be Detailed and Specific
Instead of: "Add a button"
Try: "Add a primary action button in the header that toggles between Celsius and Fahrenheit, styled with our university's blue (#003366) and white text"

### 2. Use the Question Technique
When unsure about context:
```
"I want to implement user authentication. Please ask me 3 clarifying 
questions about security requirements and user experience before suggesting code."
```

### 3. Create New Chats for New Features
- Keeps context focused
- Prevents confusion between features
- Easier to reference implementations

### 4. Iterate on Responses
Don't accept the first suggestion if it's not perfect:
- "This is good, but make the animations smoother"
- "Add more error handling to this implementation"
- "Refactor this to be more maintainable"

## Context Management Strategies

### Choosing the Right Files
1. **Always include**: The primary file you're modifying
2. **Often helpful**: Related templates, stylesheets, or modules
3. **Sometimes needed**: Configuration files (requirements.txt, docker-compose.yml)
4. **Context-specific**: Database schemas, API documentation

### Context Tips:
- Open relevant files before starting a chat
- Use the file picker to explicitly add context
- Reference specific files in your prompts
- Remove irrelevant files to reduce noise

## Advanced Tips

### Premium Requests and Billing
Each time you send a prompt in a chat window or trigger a response from Copilot, you're making a request. Some Copilot features use more advanced processing power and count as premium requests.

**Managing Premium Requests**:
- Premium request counters reset on the 1st of each month at 00:00:00 UTC.
- Monitor usage in VS Code status bar or GitHub settings
- Additional premium requests beyond your plan's included amount are billed at $0.04 USD per request.
- Set spending limits to control costs

### Response Customization
While out of scope for this workshop, be aware that GitHub Copilot supports:
- Custom instructions per repository
- Team-specific coding standards
- Automated response patterns

Learn more: https://docs.github.com/en/copilot/concepts/response-customization

## Workshop Exercises

### Exercise 1: Start Simple (30 minutes)
1. Extract CSS to external file using Edit mode
2. Change color scheme with specific hex codes
3. Update fonts using #web to find modern options

### Exercise 2: Add Functionality (45 minutes)
1. Implement dark mode with screenshot feedback
2. Add temperature conversion using Agent mode
3. Cache plot generation for performance

### Exercise 3: Go Modern (60 minutes)
1. Create new pages using Agent mode
2. Implement modern UI with detailed prompts
3. Add data filtering with complex interactions

### Exercise 4: Model Experimentation (20 minutes)
1. Try the same complex prompt with different models
2. Compare response quality and speed
3. Document which models work best for different tasks

## Common Pitfalls and Solutions

### Pitfall 1: Accepting First Suggestion
**Solution**: Always iterate! Ask for improvements or alternatives

### Pitfall 2: Losing Context
**Solution**: Manage open files carefully, use explicit file references

### Pitfall 3: Vague Prompts
**Solution**: Include specific requirements, visual descriptions, and examples

### Pitfall 4: Ignoring Premium Request Usage
**Solution**: Monitor usage regularly, use standard models when appropriate

### Pitfall 5: Not Using Visual Context
**Solution**: Leverage screenshots for UI improvements

## Expected Outcomes
After this workshop, participants will:
- Master all three Copilot Chat modes (Ask, Edit, Agent)
- Effectively use web search and image attachments
- Understand model selection and premium request management
- Write detailed, effective prompts
- Build modern web features rapidly with AI assistance

## Resources and References

### Official Documentation
- **Prompt Engineering Guide**: https://docs.github.com/en/copilot/concepts/prompt-engineering
- **Response Customization**: https://docs.github.com/en/copilot/concepts/response-customization
- **Premium Request Monitoring**: https://docs.github.com/en/copilot/how-tos/manage-and-track-spending/monitor-premium-requests

### Key Takeaways
- GitHub Copilot is a tool to enhance productivity, not replace expertise
- Effective prompting is a skill that improves with practice
- Different modes serve different purposes - choose wisely
- Visual context (screenshots) can dramatically improve results
- Model selection matters for complex tasks
- Monitor premium request usage to control costs

Remember: The goal is to work *with* AI as a collaborative partner, leveraging its strengths while applying your domain knowledge and creativity to build meaningful solutions.