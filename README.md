# Jarvis Android App

WebView-based Jarvis voice assistant with native Android microphone (SpeechRecognizer)
and Text-to-Speech, powered by the free Gemini API.

## GitHub par APK banane ke steps

1. GitHub par ek naya (empty) repository banao.
2. Is poore folder ko us repo me push karo:
   ```
   git init
   git add .
   git commit -m "Jarvis app"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```
3. Push hote hi GitHub repo ke **Actions** tab me "Build Jarvis APK" workflow apne aap chalega.
4. 2-3 minute me workflow finish hoga. Us run ko kholo, neeche **Artifacts** section me
   `jarvis-debug-apk` milega — usse download karo (zip ke andar `app-debug.apk` hai).
5. APK ko phone me transfer karke install karo (Settings > "Install unknown apps" allow karna
   padega, kyunki ye Play Store se nahi hai).

## Pehli baar app kholne par
- Mic permission allow karo.
- Andar diye box me apni free Gemini API key daalo (https://aistudio.google.com/app/apikey se lo) aur Save dabao.
- Mic dabao, bolo — "time batao", "google kholo cricket score", "youtube kholo lofi songs",
  ya koi bhi general sawal seedha Gemini se pooch lo.

## Signed / Play Store release APK chahiye to
Is workflow me `assembleDebug` ki jagah `assembleRelease` use karo aur apna keystore
GitHub Secrets me daal kar signing config `app/build.gradle` me add karo — agar chaho to
bata dena, main woh bhi set kar dunga.
