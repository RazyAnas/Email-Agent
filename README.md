<h1>📧 Email Campaign & Click Tracking using n8n</h1>

<p>
This project demonstrates how to build a <strong>GoPhish-style email campaign system</strong>
using <strong>n8n Cloud / Self-hosted n8n</strong>, Google Sheets, SMTP, and Webhooks.
</p>

<div class="box">
  <strong>Use cases:</strong>
  <ul>
    <li>Security awareness campaigns</li>
    <li>Internal phishing simulations</li>
    <li>Email click tracking</li>
    <li>Marketing or compliance testing (authorized only)</li>
  </ul>
</div>

---

<h2>🧩 What’s Included</h2>

<ul>
  <li><strong>Email Campaign Workflow (JSON)</strong>
    <ul>
      <li>Reads users from Google Sheets</li>
      <li>Generates unique tracking URLs</li>
      <li>Sends HTML emails via SMTP</li>
    </ul>
  </li>
  <li><strong>Email Click Tracker Workflow (JSON)</strong>
    <ul>
      <li>Webhook-based click tracking</li>
      <li>Normalizes click data</li>
      <li>Logs clicks to Google Sheets</li>
      <li>Redirects user after click</li>
    </ul>
  </li>
</ul>

---

<h2>📁 Repository Structure</h2>

<pre>
/
├── email_campaign_workflow.json
├── email_click_tracker_workflow.json
└── README.html
</pre>

---

<h2>⚙️ Requirements</h2>

<ul>
  <li>n8n (Cloud or Self-hosted)</li>
  <li>Google Sheets account</li>
  <li>SMTP credentials (Gmail, SES, Zoho, etc.)</li>
</ul>

---

<h2>📊 Google Sheets Setup</h2>

<h3>Recipients Sheet</h3>

<pre>
email | name | status | last_sent
</pre>

<h3>Click Logs Sheet</h3>

<pre>
email | campaign_id | tracking_id | event | ip | user_agent | timestamp
</pre>

⚠️ Column names are <strong>case-sensitive</strong> and must match exactly.

---

<h2>🚀 How to Import Workflows</h2>

<div class="box">
  <ol>
    <li>Open n8n → Workflows</li>
    <li>Click <strong>Import</strong></li>
    <li>Import the JSON files from this repository</li>
    <li>Update credentials (SMTP & Google Sheets)</li>
    <li>Activate the workflows</li>
  </ol>
</div>

---

<h2>🔗 How Tracking Works</h2>

<ol>
  <li>Email contains a unique tracking URL</li>
  <li>User clicks the link</li>
  <li>Webhook receives query parameters</li>
  <li>Click data is normalized</li>
  <li>Data is appended to Google Sheets</li>
  <li>User is redirected to a landing page</li>
</ol>

---

<h2>🧪 Test vs Production Webhooks</h2>

<div class="warning">
  <strong>Important:</strong>
  <ul>
    <li><code>/webhook-test/</code> → Debugging only</li>
    <li><code>/webhook/</code> → Production (emails must use this)</li>
    <li>Workflow must be <strong>ACTIVE</strong> for production</li>
  </ul>
</div>

---

<h2>🔐 Legal & Ethical Notice</h2>

<div class="warning">
  This project is intended for <strong>authorized testing, education, and awareness</strong> only.
  <br />
  Do not use this system for:
  <ul>
    <li>Unauthorized phishing</li>
    <li>Fraud or impersonation</li>
    <li>Violating privacy laws</li>
  </ul>
  You are responsible for compliance with applicable laws and policies.
</div>

---

<h2>✨ Features</h2>

<ul>
  <li>✔ Unique per-user tracking links</li>
  <li>✔ Google Sheets as database</li>
  <li>✔ SMTP-based email delivery</li>
  <li>✔ Cloud-compatible (no Data Store)</li>
  <li>✔ Redirect after click</li>
  <li>✔ GoPhish-style architecture</li>
</ul>

---

<h2>📌 Future Improvements</h2>

<ul>
  <li>Email open tracking (pixel)</li>
  <li>Duplicate click prevention</li>
  <li>Campaign dashboards</li>
  <li>Auto follow-up emails</li>
</ul>

---
# Watch Video For More Information.
[![YouTube Video](https://img.youtube.com/vi/TTbqt7PiBpw/0.jpg)](https://youtu.be/TTbqt7PiBpw?feature=shared)


# Available Our [Hacking Course](https://linuxndroid.in)

<hr>
---

<footer>
  <p>
    Built with ❤️ using n8n<br />
    Shared for learning & awareness purposes.
  </p>
</footer>

</body>
</html>
