# NLP Tokenizer & 3D Word Embedding Visualizer

An educational, interactive web application built with HTML5, CSS3, JavaScript, and Three.js for visualizing text tokenization, vocabulary management, and 3D word embedding spaces.

## ✨ Features

1. **Interactive Text Tokenizer**
   - Real-time tokenization as you type or paste text.
   - Text normalization: lowercase conversion and punctuation stripping.
   - Deterministic color coding and sequential Token ID assignment.
   - Formatted encoded numerical array representation (e.g., `[4, 0, 1, 2, 3, 4, 5, 1, 2]`) with one-click copy.

2. **Vocabulary Lexicon Builder**
   - Automatically builds vocabulary from processed sentences.
   - Frequency counters with visual occurrence bars.
   - Search by word or Token ID, sort by ID, frequency, or alphabetical.
   - JSON export and import capabilities.
   - Persisted in browser `localStorage`.

3. **Sentence Encoder & Decoder**
   - Encode test sentences against the learned vocabulary.
   - Visual highlighting of `<UNK>` (Unknown) tokens.
   - Option to automatically learn and assign vectors to unknown words.
   - Decoder to reconstruct sentences from comma-separated Token ID arrays.

4. **3D Word Embedding Visualization (Three.js)**
   - Interactive 3D vector space rendered with Three.js.
   - High-DPI billboard text labels facing the camera.
   - Orbit controls: rotate, pan, and zoom.
   - Dynamic similarity edges between words whose cosine similarity exceeds the adjustable threshold.
   - Interactive Raycasting: hover HUD tooltips and click-to-select.
   - Direct 3D node dragging to relocate vectors in real time.

5. **Cosine Similarity Geometry Engine**
   - Calculates mathematical cosine similarity: $\cos(A, B) = \frac{A \cdot B}{\|A\| \times \|B\|}$.
   - Shows dot product, vector magnitudes, angle in degrees ($\theta^\circ$), and visual color-coded meter.
   - Top 5 closest semantic neighbors list.
   - "Beam in 3D" action that connects vectors with an animated laser in the 3D space.

6. **Manual Vector Editor & Semantic Anchor**
   - Add new words with custom $(X, Y, Z)$ coordinates.
   - "Connect to Semantic Anchor" option to place words near related concepts.
   - Edit node coordinates via sliders or live modal.
   - Duplicate prevention with instant focus on existing tokens.

7. **Live Statistics Dashboard**
   - Total Unique Words ($|V|$ size).
   - Total Tokens Processed.
   - Lexical Diversity / Type-Token Ratio (TTR %).
   - Active 3D Similarity Links.

8. **Vercel Protected Access Gate (API Key)**
   - Access guard requiring an API Key (supports Groq API keys `gsk_...`, custom passkeys, or an instant sandbox demo key).
   - Integrated Groq Llama 3 AI Corpus Generator for synthetic NLP training sentences when a Groq key is provided.

## 🚀 Deployment to Vercel

### Option 1: Deploy with Vercel CLI
```bash
npm i -g vercel
vercel
```

### Option 2: Deploy via GitHub
1. Push this folder to a GitHub repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit of NLP Tokenizer & 3D Embedding Visualizer"
   git branch -M main
   git remote add origin <your-repo-url>
   git push -u origin main
   ```
2. Import the repository into [Vercel](https://vercel.com) and click **Deploy**.
3. It will deploy as a fast static site immediately using `index.html`.
