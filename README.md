# hAI.SpeziMezzotest

Collection of fun test / blind-test web projects.

## 🎮 Projects

### Cola-Fanta Blindtest

A playful blind-taste comparison game — can you tell Cola from Fanta?

**Play:** Open `cola-fanta-blindtest.html` directly in any browser — no server required.

```bash
# Or serve locally
python3 -m http.server 8080
# Then open http://localhost:8080/cola-fanta-blindtest.html
```

## 📂 Project Structure

```
hAI.SpeziMezzotest/
├── cola-fanta-blindtest.html   # Blindtest game (standalone HTML)
├── docs/                      # Additional documentation
└── .github/
    └── workflows/
        └── trufflehog.yml    # Secret scanning
```

## 🔐 Security

This repo is scanned with [TruffleHog](.github/workflows/trufflehog.yml) for leaked secrets on every push.

## 📜 License

MIT – see [LICENSE](LICENSE)
