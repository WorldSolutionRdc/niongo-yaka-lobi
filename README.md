cat > README.md << 'EOF'
# Proxy Nginx pour VPS (167.99.88.149)

Proxy Nginx déployé sur Google Cloud Run pour rediriger le trafic TCP vers le VPS principal.

## Configuration
| Élément | Valeur |
|---------|--------|
| **VPS cible** | `167.99.88.149:443` |
| **Port d'écoute proxy** | `8080` |
| **Région VPS** | `europe-west3` (Francfort, Allemagne) |
| **Région Cloud Run** | `europe-west3` (Francfort, Allemagne) |
| **Type de proxy** | TCP Stream (Layer 4) |

## Déploiement
```bash
gcloud run deploy ultra-speed-proxy \
  --source . \
  --platform managed \
  --region europe-west3 \
  --allow-unauthenticated \
  --port 8080 \
  --memory 512Mi \
  --cpu 1 \
  --timeout 3600