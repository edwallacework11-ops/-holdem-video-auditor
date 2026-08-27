# Hold'em Video Auditor

No-Mac web prototype for iPhone screen recordings and previous hand history.

## Modes
- New Recording: analyze one new iPhone screen recording.
- Past History:
  - batch old screenshots
  - batch old screen recordings
  - CSV or JSON imports
- Audit: one merged hand database with export.

## Recognition
The app is calibrated to the supplied 709x1536 portrait Sportsbetting.ag Casino Hold'em layout.

It ships with seed templates extracted from the three supplied screenshots. Those cover only the cards seen in those screenshots. Unknown-card crops are placed in a small trainer so the user can label them once; those templates are retained in local browser storage.

This is an MVP, not yet a production-grade 52-card vision model.

## Privacy
Video/image analysis is performed in the browser. The static app has no server-side upload code.

## Important limit
It cannot log into the casino or retrieve account history on its own. Historical data must be provided as screenshots, screen recordings, or an export.

## Using on iPhone
Host this folder on any HTTPS static host and open it in Safari. The browser may pause or terminate long video analysis if the phone is locked or Safari is backgrounded, so keep the page open while processing.

## Recommended next upgrade
Replace template matching with a full 52-class model trained on the exact card art. Then add a poker-hand evaluator and result inference.
