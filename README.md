## Overview
PromptTester is a portable, BYOK (Bring Your Own Key), single-file HTML app for defining, testing, and refining LLM prompts. Think about it as Postman for LLMs.

## Features
- **Single File:** Runs entirely from one HTML file in the browser for maximum portability. Thanks for OpenAI and Gemini for no CORS restrictions.
- **OpenAI and Gemini Support:** Supports OpenAI (Completions and Requests) and Gemini APIs.
- **Nunjucks Templates:** Dynamic templating across LLM requests, prompts, and messages.
- **Variables:** Global and test-specific variables to power templates.
- **Test Management:** Define test cases with expected responses for automated validation.
- **Run History:** Track execution times and pass/fail status of previous runs.
- **Import/Export:** Save and load test configurations.
