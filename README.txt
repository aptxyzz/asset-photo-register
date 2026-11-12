Asset Photo Register v5 - Android export fix

Export is now two-stage:
1. Export Inspection ZIP prepares the package.
2. When the ZIP Ready screen appears, tap Save / Share Inspection ZIP.

The second tap is required because Android/Chrome permits native file sharing only during a direct user action. This avoids losing the share permission while the app is asynchronously reading photos and building the ZIP.

ZIP content: Asset_Register.csv, Photo_Register.csv, and all captured photos arranged in folders.
