<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# Run and deploy your AI Studio app

This contains everything you need to run your app locally.

View your app in AI Studio: https://ai.studio/apps/26e0084c-3cc2-4c0f-abc3-9777c1ce32c4

## Run Locally

**Prerequisites:**  Node.js


1. Install dependencies:
   `npm install`
2. Set the `GEMINI_API_KEY` in [.env.local](.env.local) to your Gemini API key
3. Run the app:
   `npm run dev`
   

## Troubleshooting Gemini API 403 Errors

If you encounter a `PERMISSION_DENIED` (403) error when scanning CVs with the message about "temporary service disruptions" and "unrestricted keys," you must restrict your Gemini API key in the Google Cloud Console.

### How to Fix:
1. Go to the [Google Cloud Console Credentials page](https://console.cloud.google.com/apis/credentials).
2. Find the API key you are using for `VITE_GEMINI_API_KEY`.
3. Click on the key name to edit its settings.
4. Under **API restrictions**, select **Restrict key**.
5. From the dropdown, search for and select **Generative Language API**.
6. Click **Save**.

*Note: It may take up to a few hours for these changes to propagate across Google's servers.*
