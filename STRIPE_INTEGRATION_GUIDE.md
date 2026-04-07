# Stripe Payment Integration for 68RFE Pro

## Setup Steps

### 1. Install Dependencies
```bash
npm install stripe @stripe/react-stripe-js @stripe/js express
```

### 2. Get Stripe API Keys
- Go to https://dashboard.stripe.com
- Navigate to Developers → API Keys
- Copy your **Publishable Key** and **Secret Key**

### 3. Configure Environment Variables

Create a `.env.local` file in your project root:

```env
VITE_STRIPE_PUBLIC_KEY=pk_test_YOUR_KEY_HERE
STRIPE_SECRET_KEY=sk_test_YOUR_KEY_HERE
```

**DO NOT** commit `.env.local` to Git. Add it to `.gitignore`:

```
.env.local
.env
.env.*.local
```

### 4. Use the Payment Component

In your React component:

```tsx
import StripePayment from './components/StripePayment';

export default function BuyDiagnostic() {
  return (
    <StripePayment
      amount={29.99}
      description="68RFE Pro Diagnostic Package"
      onSuccess={() => alert('Payment successful!')}
    />
  );
}
```

### 5. Test Payment

Use Stripe's test cards:
- **Card Number**: `4242 4242 4242 4242`
- **Expiry**: Any future date (e.g., `12/25`)
- **CVC**: Any 3 digits (e.g., `123`)

### 6. Production Deployment

Before going live:
1. Switch to **Live Keys** in Stripe Dashboard
2. Update environment variables with live keys
3. Enable HTTPS on your domain
4. Test with real transactions
5. Monitor Stripe Dashboard for transactions

## Files Added

- ✅ `src/components/StripePayment.tsx` - Payment form component
- ✅ `src/server/stripe.ts` - Backend API handlers
- ✅ `STRIPE_SETUP.md` - Detailed documentation
- ✅ Updated `package.json` with Stripe libraries

## Next Steps

1. Add your Stripe keys to `.env.local`
2. Run `npm install` to install dependencies
3. Integrate `<StripePayment />` component into your app
4. Create backend endpoints to handle payments
5. Set up webhook listeners for payment events

Need help? Check the [Stripe React documentation](https://stripe.com/docs/stripe-js/react)
