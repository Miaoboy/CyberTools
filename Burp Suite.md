![image](https://github.com/user-attachments/assets/0407b7ac-eeec-420c-a8a6-59a101d7b9fe)

## 1. Target
```
Purpose:
The Target tab is where you define the scope of your testing and manage the results of your interactions with the target application. It serves as the central map of the application's structure, showing all the discovered endpoints, directories, and files.

Features:
Site Map:
Displays a hierarchical map of all the endpoints in the target application.
Helps identify key resources such as APIs, admin pages, and potential attack vectors.
Scope Definition:
Allows you to specify which parts of the application you want to test.
Ensures that Burp tools (like the Spider, Scanner, etc.) operate only within the defined scope.
Request/Response Review:
You can click on any endpoint to view the HTTP requests and responses.
Helps analyze the structure, parameters, and potential vulnerabilities.
Use Case:
Use the Target tab to plan your testing, organize your findings, and focus on areas of interest (e.g., admin panels or sensitive directories).
```
## 2. Proxy
```
Purpose:
The Proxy tab is Burp Suite's core interception tool. It acts as a man-in-the-middle (MITM) proxy, intercepting and modifying traffic between your browser and the target application.

Features:
Intercept Mode:
Allows you to pause HTTP requests and responses, view their contents, and modify them before they are sent.
HTTP History:
Logs all intercepted requests and responses for analysis.
Useful for finding sensitive data, headers, and parameters.
WebSocket Messages:
Captures WebSocket traffic for applications that use real-time communication.
Use Case:
Use the Proxy tab to:

Analyze requests and responses in real time.
Modify traffic to test how the application handles unexpected input or edge cases.
Discover hidden parameters or debug application behavior.
How to Use:
Configure your browser to use Burp Suite as a proxy.
Enable Intercept to capture and modify traffic.
Review the traffic in HTTP history for further analysis.
```

## 3. Intruder
```
Purpose:
The Intruder tool is used for automated attacks such as brute-forcing, fuzzing, or manipulating parameters to test for vulnerabilities.

Features:
Payload Positions:
You define which parts of the request (e.g., parameters, headers) should be targeted for testing.
Payload Types:
Supports various payloads like wordlists, numbers, or custom values.
Attack Types:
Sniper: Tests one payload at a time (single variable testing).
Battering Ram: Reuses the same payload for all positions.
Pitchfork: Tests multiple payloads simultaneously in parallel.
Cluster Bomb: Tests all combinations of payloads across positions.
Use Case:
Use the Intruder to:

Brute-force credentials by testing combinations of usernames and passwords.
Test for injection vulnerabilities by sending various payloads (e.g., SQL injection, XSS).
Fuzz parameters to discover hidden functionality or vulnerabilities.
How to Use:
Send a request from the Proxy or Target tab to Intruder.
Define the payload positions and types.
Start the attack and review the results for anomalous behavior or responses.
```

## 4. Repeater
```
Purpose:
The Repeater tool is used for manual testing by allowing you to send the same request repeatedly with modifications. It’s ideal for fine-tuning payloads or validating vulnerabilities.

Features:
Request Modification:
You can edit HTTP requests (headers, parameters, or body) directly.
Manual Testing:
Unlike Intruder, Repeater doesn’t automate testing, making it suitable for focused, precise testing.
Response Comparison:
View and compare responses for different payloads.
Use Case:
Use the Repeater to:

Test how the application responds to specific payloads.
Validate manual exploits for vulnerabilities like SQL injection or XSS.
Debug application functionality by tweaking parameters or headers.
How to Use:
Send a request from Proxy or Target to Repeater.
Modify the request as needed.
Send the modified request and review the response.
```
