import open

# Set your OpenAI API key
open.api_key = '321234'

# Text to be translated
english_text = "Hello, how are you?"

# Provide a prompt and get a model-generated response
response = openai.Completion. create(
    engine="text-DaVinci-003",  # You can experiment with different engines
    prompt=f"Translate the following English text to French: '{english_text}'",
    max_tokens=150  # Set as needed
)

# Extract the generated text from the response
generated_text = response['choices'][0]['text']

print(generated_text)

