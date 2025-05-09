
# AI related lingo
## LLM Text to Machine
`Text(sentence/words) -> Tokenization -> Token IDs -> Embeddings (Vectors)`

Text: Input full sentence
Token: a piece of a sentence (word/character)
Tokenization: The break down of sentences in to tokens
- Example: "Hello world!" = `["Hello", "world", "!"]`
Token IDs: a number representing a token
- Example: "Hello" → 15496, "world" → 2157, "!" → 0
Vectors: a list of numbers that represent a point in space like `[1, -2, 3]`
Embeddings: A vector of numbers that represents a token in a way a model understands
- Example: 15496 → [0.25, -0.11, 0.78, ..., 0.02] where 15496 is the Token ID for "Hello"

### OpenAI Tokenizer
Check out the OpenAI Tokenizer for examples on how tokenization works within ChatGPT: [Tokenizer](https://platform.openai.com/tokenizer)

---    
# ML Process
High level view of what this looks like:
Get data -> Dataset preprocessing (cleaning the data) -> Data transformation -> Train Model -> Test Model

## Data
You need to acquire a data set to train the model. The higher quality data, the better the model will perform.

### Data Preprocessing
- Check and fix missing/invalid values in the data. Often done by either dropping that data point or imput a missing value using the mean/average of the other values related to that feature/data point.
- Check and remove duplicates
- When dealing with text:
  - lower case all the text so the casing doesn't skew the model and treats all words equally.
  - Remove certain punctuation marks, but keep others like "$" and "!" that might give additional context.
- Data split into Train + Test: Some datasets are not split into train and test, you may have to split them yourself.

### Data Transformation
The process of changing your raw data into a format that's easier for a model to understand and learn from (Models understand numbers not text, thus it needs to be converted). It helps speed up learning and improves accuracy. In a nutshell: transforming data is reshaping it into a math-friendly representation.

