# LottoInsight - South African Lotto Predictor

> AI-driven lottery analysis platform with real-time draw results, probability heatmaps, and intelligent line generation.

![Status](https://img.shields.io/badge/status-design--phase-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Version](https://img.shields.io/badge/version-0.1.0-orange)

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
- [Development](#development)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [Support](#support)

## 🎯 Project Overview

LottoInsight is a premium mobile application that leverages statistical analysis and machine learning to help users make data-driven decisions about lottery number selection. The platform combines real-time draw results, historical data analysis, and predictive modeling to provide probability heatmaps and intelligent line recommendations.

### Core Offering
- **Live Draw Results**: Real-time South African Lotto, Plus 1, and Plus 2 results
- **Probability Engine**: AI-driven predictions based on 10,000+ historical draws
- **Analytics Dashboard**: Hot/cold number tracking, gap analysis, and frequency charts
- **Line Management**: Save, track, and analyze your lottery lines
- **Premium Subscription**: Unlimited predictions and advanced analytics

## ✨ Features

### Current (Designed)
- ✅ Beautiful dark-mode UI with Material Design 3
- ✅ Real-time draw countdown timer
- ✅ Live results display with payouts
- ✅ Probability heatmap visualization
- ✅ Hot/cold number analysis
- ✅ Prediction confidence scoring
- ✅ Draw history with detailed statistics
- ✅ Settings and configuration panel
- ✅ Subscription management interface
- ✅ Ticket scanning with AR detection

### In Development
- 🔨 Backend API (Node.js/Express)
- 🔨 Database layer (PostgreSQL)
- 🔨 Web scraper for live results
- 🔨 Payment processing (PayPal integration)
- 🔨 Push notifications
- 🔨 User authentication

### Planned
- 📅 Mobile app (React Native/Flutter)
- 📅 Advanced ML predictions
- 📅 Community features
- 📅 Social sharing
- 📅 Advanced analytics export

## 🛠️ Tech Stack

### Frontend
- **Framework**: React Native / Flutter (planned)
- **Web Version**: React + TypeScript
- **Styling**: Tailwind CSS + Material Design 3 tokens
- **State Management**: Redux / Riverpod (planned)
- **UI Components**: Custom component library

### Backend
- **Runtime**: Node.js v18+ / Python 3.10+
- **Framework**: Express.js / FastAPI
- **Database**: PostgreSQL 14+
- **API**: RESTful with OpenAPI documentation
- **Authentication**: JWT tokens
- **Payments**: PayPal SDK

### DevOps
- **Container**: Docker & Docker Compose
- **CI/CD**: GitHub Actions
- **Deployment**: AWS / Heroku / DigitalOcean
- **Monitoring**: CloudWatch / Datadog (planned)
- **Scraping**: Puppeteer / BeautifulSoup

## 🏗️ Architecture

### System Overview

```
┌─────────────────────────────────────────────────────────┐
│                   LottoInsight System                     │
└─────────────────────────────────────────────────────────┘

┌──────────────┐      ┌──────────────┐      ┌──────────────┐
│   Frontend   │      │   Backend    │      │   Scraper    │
│   (React)    │◄────►│   (Node.js)  │◄────►│   (Python)   │
└──────────────┘      └──────────────┘      └──────────────┘
                            │
                            │
                      ┌─────▼─────┐
                      │ PostgreSQL │
                      │ Database   │
                      └───────────┘

┌──────────────────────────────────────────┐
│   External Services                      │
│  • PayPal (payments)                     │
│  • SARS Lotto API / Web Scraper          │
│  • AWS S3 (storage)                      │
│  • SendGrid (email)                      │
└──────────────────────────────────────────┘
```

### Data Flow

1. **Scraper** → Fetches lottery results from official sources
2. **API** → Processes and stores data in PostgreSQL
3. **Frontend** → Queries API for display and analysis
4. **Webhook** → Notifies users of new results

## 🚀 Getting Started

### Prerequisites

- Node.js v18+ or Python 3.10+
- Docker & Docker Compose
- Git
- PostgreSQL 14+ (or use Docker)
- PayPal Developer Account

### Quick Start

#### 1. Clone the Repository

```bash
git clone https://github.com/ruca3333/LOTTO-INSIGHT.git
cd LOTTO-INSIGHT
```

#### 2. Set Up Environment

```bash
# Copy environment template
cp .env.example .env

# Edit with your credentials
nano .env
```

#### 3. Start with Docker

```bash
docker-compose up -d
```

#### 4. View Frontend

Open `http://localhost:3000` in your browser.

### Manual Setup (Without Docker)

#### Backend

```bash
cd backend
npm install
npm run dev
```

#### Frontend

```bash
cd frontend
npm install
npm start
```

#### Scraper

```bash
cd scraper
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python main.py
```

## 💻 Development

### Project Structure

```
LOTTO-INSIGHT/
├── docs/                          # Documentation
│   ├── API.md                     # API specification
│   ├── ARCHITECTURE.md            # System architecture
│   ├── HIRING.md                  # Hiring guide
│   └── DEPLOYMENT.md              # Deployment guide
├── designs/                       # UI/UX designs
│   ├── dashboard.html
│   ├── predictions.html
│   ├── analytics.html
│   └── ...                        # All 13 screens
├── frontend/                      # React application (planned)
│   ├── src/
│   ├── public/
│   └── package.json
├── backend/                       # Node.js API
│   ├── src/
│   ├── tests/
│   └── package.json
├── scraper/                       # Python web scraper
│   ├── src/
│   ├── tests/
│   └── requirements.txt
├── docker-compose.yml
├── .env.example
├── .github/
│   ├── workflows/                 # CI/CD pipelines
│   └── ISSUE_TEMPLATE/
└── README.md
```

### Workflow

1. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

2. **Make changes and commit**
   ```bash
   git commit -m "feat: add hot number tracking"
   ```

3. **Push and create a Pull Request**
   ```bash
   git push origin feature/your-feature-name
   ```

4. **Code review and merge**

### Running Tests

```bash
# Backend tests
cd backend && npm test

# Scraper tests
cd scraper && pytest
```

### Code Standards

- **Formatting**: Prettier (JavaScript), Black (Python)
- **Linting**: ESLint (JavaScript), Pylint (Python)
- **Commits**: Conventional Commits

## 📦 Deployment

### Development

```bash
docker-compose -f docker-compose.dev.yml up
```

### Staging

```bash
docker-compose -f docker-compose.staging.yml up
```

### Production

See [DEPLOYMENT.md](docs/DEPLOYMENT.md) for full instructions.

```bash
docker-compose -f docker-compose.prod.yml up -d
```

## 🤝 Contributing

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/amazing-feature`)
3. **Commit your changes** (`git commit -m 'feat: add amazing feature'`)
4. **Push to the branch** (`git push origin feature/amazing-feature`)
5. **Open a Pull Request**

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## 📚 Documentation

- **[API Documentation](docs/API.md)** - Complete API reference
- **[Architecture Guide](docs/ARCHITECTURE.md)** - System design and data flow
- **[Scraper Implementation](docs/SCRAPER.md)** - Web scraping guide
- **[Deployment Guide](docs/DEPLOYMENT.md)** - How to deploy to production
- **[Hiring Guide](docs/HIRING.md)** - Finding and vetting developers
- **[Design System](docs/DESIGN_SYSTEM.md)** - UI tokens and components

## 🔐 Security

- All API calls use HTTPS
- Sensitive data stored in `.env` (never committed)
- Database credentials encrypted
- PayPal integration uses OAuth 2.0
- User input validated on both frontend and backend

See [SECURITY.md](docs/SECURITY.md) for full security policy.

## 📈 Roadmap

### Phase 1: MVP (Months 1-3)
- ✅ Design system finalized
- 🔨 Backend API complete
- 🔨 Web scraper operational
- 🔨 Database schema finalized

### Phase 2: Mobile & Payments (Months 4-6)
- 📅 React Native app
- 📅 PayPal integration
- 📅 Push notifications
- 📅 User authentication

### Phase 3: Advanced Features (Months 7-9)
- 📅 ML predictions
- 📅 Community features
- 📅 Advanced analytics
- 📅 Social sharing

### Phase 4: Scale & Optimization (Months 10-12)
- 📅 Performance tuning
- 📅 Global expansion
- 📅 Multi-country support
- 📅 Advanced monetization

## 💰 Pricing

**Free Tier**
- Basic dashboard
- Last 10 draws
- Limited predictions

**Premium (R120 lifetime / $9.99/month)**
- Unlimited predictions
- Full analytics
- Advanced heatmaps
- Priority support
- No ads

## 🐛 Issues & Support

Found a bug? Have a feature request?

1. **Search existing issues**: https://github.com/ruca3333/LOTTO-INSIGHT/issues
2. **Create a new issue**: Include:
   - Detailed description
   - Steps to reproduce
   - Expected vs actual behavior
   - Screenshots if applicable

**Email Support**: support@lottoinsight.app (coming soon)

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details

## 👨‍💼 Team

**Project Lead**: ruca3333 (@ruca3333)

**Looking for**: 
- Full-stack developers
- Backend engineers
- Mobile developers
- DevOps engineers

See [HIRING.md](docs/HIRING.md) for how to join.

## 🙏 Acknowledgments

- Material Design 3 for design tokens
- South African Lotto for historical data
- All contributors and supporters

## 📞 Contact

- **GitHub Issues**: [Report bugs](https://github.com/ruca3333/LOTTO-INSIGHT/issues)
- **GitHub Discussions**: [Ask questions](https://github.com/ruca3333/LOTTO-INSIGHT/discussions)
- **Email**: contact@lottoinsight.app (coming soon)

---

**Built with ❤️ in South Africa**

Last Updated: 2026-05-08