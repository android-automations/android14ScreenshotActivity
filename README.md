ScreenshotService Class:
The ScreenshotService is a foreground service and must be initialized properly before it can capture screenshots. Screenshot permission must be granted by the user before it can initiate the capture process.

Usage:
Initialization: Before using the ScreenshotService to capture screenshots, ensure that it is properly initialized. Initialization involves starting the service and acquiring necessary permissions.

Screenshot Permission: Before sending the ACTION_RECORD intent to the ScreenshotService, make sure that the application has obtained screenshot permission from the user. Without this permission, the service won't be able to capture screenshots successfully.

Handling Image Frames: The ScreenshotService utilizes the ImageTransmogrifier class (it) to handle individual frames as they become available from the OnImageAvailable() method.

nonSharedData: This data class is used for storing various values and states within the application. It includes flags indicating whether screenshot permission has been granted and holds the latest bitmap retrieved from the screen, providing easy access throughout the app.
