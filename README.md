# StudyBridge

StudyBridge helps a learner locate relevant passages in notes without sending the text to an AI server. It embeds the notes and question in the browser using `Xenova/all-MiniLM-L6-v2` via Transformers.js, ranks passages by cosine similarity, and shows the original text so the learner can check context.

## Run

Serve this folder over HTTP, for example `python -m http.server 8000`, and open `http://localhost:8000`. The first model download requires an internet connection; subsequent use depends on browser caching. Press **Try sample notes**, prepare them, and ask a question.

The results are retrieval matches, not factual answers. Similarity is not a measure of truth. The model is English-focused; very long notes are capped at 30,000 characters and 80 passages. The model and library are fetched from Hugging Face and jsDelivr. Notes are processed locally and are not persisted.

## Credits and AI disclosure

The sentence embedding model is Xenova/all-MiniLM-L6-v2, distributed by Hugging Face. The app uses Hugging Face Transformers.js and ONNX Runtime Web. OpenAI Codex assisted with design and implementation; contributors must be accurately disclosed in any submission.

Target: STEM2Connect education track. No entry has been submitted.
