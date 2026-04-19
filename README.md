1.Digital Bodyguard
A smart, context-aware toxicity filter for video game chats.

If you've ever played an online multiplayer game, you know how toxic the chat can get. The problem with standard chat filters is that they are dumb—they flag normal gamer slang as "toxic" and completely miss actual harassment if the troll spells a word slightly wrong.

Digital Bodyguard fixes this using a two-layer hybrid AI approach. It catches the obvious garbage instantly, and uses a Deep Learning brain to read the room for context and sarcasm.

2. How It Works Under the Hood
To make sure this filter is both fast and accurate, the architecture is split into two layers:

The Fast Intercept (Lexical Rules): A high-speed Layer 1 engine that immediately catches and blocks severe, zero-tolerance vocabulary before it even reaches the AI.

The Context Engine (Bi-LSTM): If a message passes Layer 1, it goes to a PyTorch Bidirectional LSTM. Because it reads the sentence both forwards and backwards, it actually understands the context of the message, not just the individual words.

The Vocabulary (GloVe): Instead of making the AI learn English from scratch, it's pre-loaded with Stanford's GloVe (6B-100d) word embeddings.

The Interface: A clean, responsive front-end built in Streamlit so users can actually test the model live.


Try It Yourself
Want to test the bodyguard? Run it locally:

Install the required Python libraries:
pip install torch torchtext pandas streamlit

Boot up the Streamlit interface:
streamlit run app.py
