## Overview
PromptTester is a portable, BYOK (Bring Your Own Key), single-file HTML app for defining, testing, and refining LLM prompts. Think about it as Postman for LLMs.

## Features
- **Single File:** Runs entirely from one HTML file in the browser for maximum portability. Thanks for OpenAI and Gemini for no CORS restrictions.
- **Multi-LLM Provider Support:** Supports OpenAI (Completions and Requests) and Gemini APIs. Easy to add more LLM providers.
- **Raw Payloads:** Parses raw OpenAI and Gemini payloads, automatically extracts the prompt and the messages.
- **Nunjucks Templates:** Dynamic templating across LLM requests, prompts, and messages.
- **Variables:** Global and test-specific variables to power templates.
- **Tests:** Define test cases with expected responses for automated validation.
- **AI-assisted evaluation (judge):** Uses AI to evaluate the response of the LLM and compare it with the expected response.
- **Run History:** Track execution times and pass/fail status of previous runs.
- **Import/Export:** Save and load test configurations.
