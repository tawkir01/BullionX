# KishanMitra

KishanMitra is a mobile-first tomato leaf demo that presents possible crop issues and a practical, safety-focused solution plan. The current classifier is a mock; it is not a trained model or a confirmed diagnosis.

## Run locally

```sh
npm install
npm run dev
```

Run the production build and plan safety tests with:

```sh
npm run build
npm test
```

## Solution guidance

Disease playbooks and five-phase action plans live in `public/data/guidance_table.json`. Entries are marked unverified and intended for local agricultural expert review. Chemical entries are empty and remain locked unless confidence, farmer confirmation, and local verification are all present. The interface directs farmers to an agri officer / KVK for local treatment options.

Weather and mandi context are explicitly marked synthetic and may be stale; they are not live information. Scenario metadata and context data are served from `public/data/`. The web app caches its shell and guidance records for offline reading after the first successful load. Photos are resized and compressed on-device and checked for basic exposure and resolution only. They are not uploaded or sent to an ML service, and the demo does not validate tomato identity or diagnose disease. Candidate labels are illustrative mock results.

The Home, Demo scenarios, History, and About & safety views are available from the main navigation. Check history, draft answers, context selections, and plan progress are saved in browser local storage on the current device.
