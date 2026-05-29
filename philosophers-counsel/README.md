# The Philosopher's Counsel

A standalone web app where you can hold conversations with ten of history's greatest philosophers — each answering in their own authentic voice, vocabulary, and philosophical style.

## Philosophers

| Philosopher | Dates | School |
|---|---|---|
| Socrates | 470–399 BC | Socratic method, irony, "I know that I know nothing" |
| Aristotle | 384–322 BC | Logic, virtue ethics, the golden mean |
| Friedrich Nietzsche | 1844–1900 | Will to power, eternal recurrence, aphoristic style |
| Immanuel Kant | 1724–1804 | Categorical imperative, duty, pure reason |
| Simone de Beauvoir | 1908–1986 | Existential feminism, freedom, the Other |
| Albert Camus | 1913–1960 | Absurdism, revolt, living without appeal |
| Alan Watts | 1915–1973 | Zen, Taoism, the illusion of the separate self |
| Confucius | 551–479 BC | Ritual propriety, benevolence, social harmony |
| Daniel Dennett | 1942–2024 | Consciousness, free will, evolutionary naturalism |
| Arthur Schopenhauer | 1788–1860 | The Will, pessimism, aesthetic transcendence |

## Getting an Anthropic API Key

1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign up or log in
3. Navigate to **API Keys** in the left sidebar
4. Click **Create Key**, give it a name, and copy it
5. Paste it into the app's setup screen

The key is stored only in your browser's `localStorage` — it is never sent anywhere except directly to Anthropic's API.

## Running Locally

No build step required. Just open `index.html` in any modern browser:

```
# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html
```

Or serve it with any static file server:

```bash
npx serve .
# or
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `philosophers-counsel`)
2. Push these files to the `main` branch:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/philosophers-counsel.git
   git push -u origin main
   ```
3. In your repository, go to **Settings → Pages**
4. Under **Source**, select **Deploy from a branch**
5. Choose branch: `main`, folder: `/ (root)`
6. Click **Save**
7. After a minute or two, your app will be live at `https://YOUR_USERNAME.github.io/philosophers-counsel/`

## Usage Notes

- **API costs**: Each message uses the `claude-sonnet-4-20250514` model. Conversations are short but keep an eye on your Anthropic usage dashboard.
- **Conversation history**: The full conversation is sent with each message for coherent multi-turn dialogue. Long conversations will use more tokens.
- **Switching philosophers**: Selecting a different philosopher clears the conversation and starts fresh.
- **Privacy**: Your API key and conversations never leave your browser except as direct API calls to Anthropic.

## License

MIT — see [LICENSE](LICENSE).
