# Orbit

Voice-first AI assistant prototype built with Expo Router.

## Run in Cosyra

```bash
git clone https://github.com/fwrobens/Orbit.git
cd Orbit
npm install
npx expo install --fix
npx expo start --tunnel
```

The app offers functional local tasks and saved chat history. AI answers require a backend URL in `.env`: `EXPO_PUBLIC_ORBIT_API_URL=https://your-backend.example/chat`. This endpoint accepts `{messages:[{role,content}]}` and responds with `{reply:string}`. Never put private model API keys in public Expo environment variables.

The native speech recognition package **does not work in Expo Go**. Use an Expo development build (EAS for physical iPhone; `npx expo run:android` for a local Android environment). The voice screen displays a helpful explanation when the native module is missing.

The orb is a gradient-based prototype, not yet a custom real-time Skia shader. Calendar and third-party integrations require backend OAuth work.
