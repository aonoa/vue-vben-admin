# Web Micro Application

This is a micro-frontend main application based on `web-antd`, using [micro-app](https://micro-zoe.github.io/micro-app/) for micro-frontend architecture.

## Features

- ✅ Based on Vue 3 + Vite + Ant Design Vue
- ✅ Integrated with micro-app framework for micro-frontend support
- ✅ Can load and manage multiple sub-applications
- ✅ Independent routing and state management
- ✅ Shared dependencies and resources

## Development

```bash
# Install dependencies
pnpm install

# Start development server (port 5888)
pnpm run dev:micro

# Build for production
pnpm run build:micro

# Type checking
pnpm run typecheck
```

## Configuration

### Environment Variables

- `VITE_APP_TITLE`: Application title (default: "Vben Admin Micro")
- `VITE_APP_NAMESPACE`: Application namespace for isolation (default: "vben-web-micro")
- `VITE_PORT`: Development server port (default: 5888)

### Micro-App Configuration

The micro-app is initialized in `src/bootstrap.ts`:

```typescript
microApp.start({
  tagName: 'micro-app',
  iframe: false,
  'disable-memory-router': false,
  'disable-sandbox': false,
});
```

## Adding Sub-Applications

To add a sub-application, use the `<micro-app>` component in your views:

```vue
<micro-app 
  name="sub-app-name" 
  url="http://localhost:3000"
  :data="dataForChild"
></micro-app>
```

## Demo

A demo page is available at `/demos/micro-app` to showcase micro-frontend functionality.

## Key Differences from web-antd

1. **Package Name**: `@vben/web-micro` instead of `@vben/web-antd`
2. **Port**: Runs on port 5888 instead of 5666
3. **Namespace**: Uses `vben-web-micro` namespace
4. **Dependencies**: Added `@micro-zoe/micro-app` for micro-frontend support
5. **Bootstrap**: Initializes micro-app framework on application startup

## Learn More

- [micro-app Documentation](https://micro-zoe.github.io/micro-app/)
- [Vben Admin Documentation](https://doc.vben.pro)
