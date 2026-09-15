## Overview

PromptTester is a portable, BYOK (Bring Your Own Key), single-file HTML app for testing and evaluating LLM prompts and requests. You can think of it as Postman for LLMs.

Try it online: [https://dmytronius.github.io/prompt-tester/PromptTester.html](https://dmytronius.github.io/prompt-tester/PromptTester.html)

It can be useful for:

* Making sure your prompt works as expected 100 out of 100 times.
* Finding the best LLM setup for your use case. Change the model, temperature, reasoning level, etc., and see how these changes affect response quality and token consumption.
* Checking your prompt quality via a prompt audit.
* Debugging your LLM request.

## Features

* **Single File:** Runs entirely from a single HTML file in the browser for maximum portability. Thanks to OpenAI, Gemini, OpenRouter, and Hugging Face for having no CORS restrictions.
* **BYOK:** Your API keys are stored in the browser's local storage and are never shared with anyone.
* **Multi-LLM Provider Support:** Supports OpenAI (Completions and Responses) and Gemini APIs. More LLM providers can be added easily.
* **Tests:** Define test cases with expected responses for automated validation. Multiple tests are run in parallel to speed up testing.
* **AI Prompt Audit:** Runs a metaprompt (editable in settings) to detect conflicts, logical gaps, ambiguities, factual inaccuracies, etc., in the prompt.
* **Tools Used:** Checks whether all tools defined in the request are mentioned in the prompt.
* **AI-Assisted Evaluation (Judge):** Uses AI to evaluate the LLM's response and compare it with the expected response.
* **Run History:** Track execution times and the pass/fail status of previous runs.
* **Import/Export:** Save and load test configurations.
* **Raw Payloads:** Paste raw OpenAI or Gemini payloads, and the app will automatically extract the prompt and messages.
* **Nunjucks Templates:** Use dynamic templating across LLM requests, prompts, and messages.
* **Variables:** Use global and test-specific variables to power templates.

## Limitations

The app is intentionally kept small and simple, which comes with some limitations.

* When you switch LLM providers, you must manually change the request JSON and all other parameters (such as roles) to ones supported by the new provider.
* The messages list normally has a fixed number of messages, so tests with different conversation lengths need to be implemented using variables such as `assistant_msg1`, `usr_msg1`, `assistant_msg2`, `usr_msg2`, etc.
* Tool definitions must be provided as manual JSON.
* Structured output schema definitions must be provided as manual JSON.
