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

## 🚀 Deployment

### Portainer Stack (Recommended for Production)

Deploy the entire application as a Docker container in your Portainer environment:

```bash
# Create external network (if not exists)
docker network create highfishNetwork

# Deploy stack via Portainer UI
1. Go to Stacks → Add stack
2. Paste docker-compose.yml content
3. Name: hAI.SpeziMezzotest
4. Deploy
```

**Access:**
- **URL**: `http://<your-portainer-host>:8080`
- **Container**: `speci-mezzotest`
- **Network**: `highfishNetwork`

### Docker Standalone

```bash
# Build and run manually
docker build -t ghcr.io/jbkunama1/hai.spezimezzotest:latest .
docker run -d -p 8080:80 --name speci-mezzotest \
  --network highfishNetwork \
  ghcr.io/jbkunama1/hai.spezimezzotest:latest
```

### GitHub Pages

The application is also deployed to GitHub Pages at:
- **Live Demo**: [https://jbkunama1.github.io/hAI.SpeziMezzotest/](https://jbkunama1.github.io/hAI.SpeziMezzotest/)

*Note: GitHub Pages deployment is simplified for demo purposes.*

## 📂 Project Structure

```
hAI.SpeziMezzotest/
├── cola-fanta-blindtest.html   # Blindtest game (standalone HTML)
├── intro.html                 # Video intro page
├── role-select.html           # Role selection (Moderator/Tester/Admin)
├── admin.html                 # Admin panel for game configuration
├── Dockerfile                 # Container build configuration
├── docker-compose.yml         # Portainer stack configuration
├── .github/
│   └── workflows/
│       ├── docker-build.yml    # Build and push Docker image
│       ├── gh-pages.yml        # Deploy to GitHub Pages
│       └── trufflehog.yml     # Security scanning
└── docs/                      # Additional documentation
```

## 🔐 Security

This repo is scanned with [TruffleHog](.github/workflows/trufflehog.yml) for leaked secrets on every push.

## 📜 License

MIT – see [LICENSE](LICENSE)
