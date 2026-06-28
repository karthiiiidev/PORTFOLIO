# Vercel Speed Insights Setup

This project has been configured with Vercel Speed Insights to track and monitor web performance metrics.

## What Was Installed

- **Package**: `@vercel/speed-insights` (v2.0.0)
- **Installation Method**: npm
- **Lock File**: package-lock.json (created/updated)

## Implementation Details

### For This Vanilla HTML/JavaScript Project

Since this is a static HTML portfolio without a build process, the Speed Insights initialization code has been added directly to the `<head>` section of `index.html`:

```html
<!-- Vercel Speed Insights -->
<script>
  window.si = window.si || function () { (window.siq = window.siq || []).push(arguments); };
</script>
```

This initialization script prepares the page for Speed Insights tracking. When you deploy to Vercel with Speed Insights enabled in your dashboard, Vercel will automatically inject the necessary tracking scripts.

## Next Steps to Activate Speed Insights

1. **Enable Speed Insights in Vercel Dashboard**:
   - Go to your project settings on Vercel
   - Navigate to the "Speed Insights" section
   - Enable Speed Insights for your project

2. **Deploy Your Site**:
   - Deploy your project to Vercel using `vercel deploy` or through GitHub integration
   - Speed Insights will automatically start tracking performance metrics after deployment

3. **View Metrics**:
   - After deployment, visit your Vercel dashboard
   - Go to the "Speed Insights" tab to view performance data
   - You'll see metrics like:
     - Real Experience Score (RES)
     - First Contentful Paint (FCP)
     - Largest Contentful Paint (LCP)
     - First Input Delay (FID)
     - Cumulative Layout Shift (CLS)

## How It Works

- Speed Insights automatically tracks Core Web Vitals and other performance metrics
- Data is collected from real users visiting your site
- Metrics are aggregated and displayed in the Vercel dashboard
- The tracking script only loads on production deployments
- No data is tracked in development mode

## Configuration Options

While the current implementation uses default settings, you can customize Speed Insights by adding configuration through the `window.si` function if needed in the future. See the [official documentation](https://vercel.com/docs/speed-insights) for advanced configuration options.

## Important Notes

- Speed Insights requires your site to be deployed on Vercel
- The tracking script is automatically injected by Vercel when enabled in the dashboard
- The initialization code in `index.html` prepares your site to receive the Speed Insights script
- No build process is required for this implementation

## Resources

- [Vercel Speed Insights Documentation](https://vercel.com/docs/speed-insights)
- [Speed Insights Quickstart Guide](https://vercel.com/docs/speed-insights/quickstart)
- [@vercel/speed-insights Package](https://www.npmjs.com/package/@vercel/speed-insights)
