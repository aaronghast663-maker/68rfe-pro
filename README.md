# 68RFE Pro

**Freemium diagnostic tool for the Cummins 68RFE transmission**

## 🚀 Features

- **DTC Lookup** - Search and understand diagnostic trouble codes (Free)
- **Symptom Flowcharts** - Guided diagnosis for transmission issues (Free)
- **Clutch Specifications** - Detailed clutch pack information and specs (Free)
- **VIN Decoder** - Decode VINs to identify transmission details (Free)
- **Premium Diagnostic Packages** - Advanced analysis and detailed reports (Paid)
- **Mobile Responsive** - Works on all devices
- **Freemium Model** - Essential tools are free, premium features available

## 🛠️ Tech Stack

- **Frontend:** React 18, TypeScript, Vite, Tailwind CSS
- **Icons:** Lucide React
- **Payments:** Stripe
- **Build Tool:** Vite
- **Code Quality:** ESLint, TypeScript strict mode
- **Deployment:** GitHub Pages with GitHub Actions CI/CD

## 📦 Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/aaronghast663-maker/68rfe-pro.git
cd 68rfe-pro

# Install dependencies
npm install

# Start development server
npm run dev
```

The application will open at `http://localhost:3000`

### Building for Production

```bash
npm run build
```

Output files will be in the `dist/` directory.

### Preview Production Build

```bash
npm run preview
```

## 📝 Available Scripts

- `npm run dev` - Start development server with hot module replacement
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally
- `npm run lint` - Run ESLint code quality checks
- `npm run type-check` - Run TypeScript type checking

## 💳 Stripe Payment Setup

1. **Get API Keys:**
   - Visit https://dashboard.stripe.com
   - Copy your Publishable and Secret keys

2. **Configure Environment:**
   Create `.env.local`:
   ```env
   VITE_STRIPE_PUBLIC_KEY=pk_test_YOUR_KEY
   STRIPE_SECRET_KEY=sk_test_YOUR_KEY
   ```

3. **Test with Stripe Cards:**
   - Card: `4242 4242 4242 4242`
   - Any future expiry date
   - Any 3-digit CVC

See [STRIPE_INTEGRATION_GUIDE.md](./STRIPE_INTEGRATION_GUIDE.md) for detailed setup instructions.

## 🚀 Deployment

### GitHub Pages Automatic Deployment

This repository is configured with GitHub Actions for automatic deployment:

1. **Push to main:**
   ```bash
   git add .
   git commit -m "Your message"
   git push origin main
   ```

2. **Enable GitHub Pages:**
   - Go to Settings → Pages
   - Set source to "GitHub Actions"

3. **Monitor deployment:**
   - Check Actions tab for workflow status
   - Site will be live at: `https://aaronghast663-maker.github.io/68rfe-pro/`

## 📊 Project Structure

```
68rfe-pro/
├── src/
│   ├── components/
│   │   └── StripePayment.tsx      # Payment form component
│   ├── server/
│   │   └── stripe.ts              # Payment API handlers
│   ├── App.tsx                    # Main app component
│   ├── main.tsx                   # React entry point
│   ├── index.css                  # Global styles
│   └── App.css                    # App component styles
├── .github/
│   └── workflows/
│       └── build-and-deploy.yml   # CI/CD pipeline
├── public/
│   └── index.html                 # HTML template
├── package.json                   # Dependencies & scripts
├── vite.config.ts                 # Vite configuration
├── tsconfig.json                  # TypeScript config
├── .eslintrc.cjs                  # ESLint config
└── README.md                      # This file
```

## 🤝 Contributing

Contributions are welcome! Please feel free to:
- Report bugs or issues
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

MIT License - See LICENSE file for details

## 📞 Support

For issues, questions, or suggestions:
- Open a GitHub issue
- Check existing documentation
- Visit the live site: https://aaronghast663-maker.github.io/68rfe-pro/

## 🙏 Acknowledgments

Built with ❤️ for the Cummins diesel community.

---

**Live Site:** https://aaronghast663-maker.github.io/68rfe-pro/
**Repository:** https://github.com/aaronghast663-maker/68rfe-pro
