# PipeSentinel Chromium browser QA

PipeSentinel uses Playwright + Chromium for browser-level quality checks of the Vite/React SOC dashboard. Chromium is installed only in the test environment, not added to the production application.

The smoke suite checks page rendering, uncaught JavaScript exceptions, and horizontal overflow at mobile (390px), tablet (768px), and desktop (1365px) viewports. It does not generate events, authenticate to external systems, or perform incident-response actions. Live Socket.IO synchronization needs a separate deterministic backend fixture and is not claimed by these tests.

## Local run

Start the frontend:

```bash
cd frontend
npm ci
npm run dev
```

From the repository root in another terminal:

```bash
python -m pip install -r tests/browser/requirements.txt
python -m playwright install chromium
python -m pytest -q tests/browser
```

Set `PIPESENTINEL_BASE_URL` for a different authorised local URL. These are smoke tests, not a security assessment or full real-time integration test.
