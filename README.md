# Ak-earn-money-<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ak Money</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>Welcome to Ak Money</h1>
    <p>Your trusted platform for easy money transactions.</p>
  </header>
  <main>
    <section class="deposit-section">
      <h2>Deposit Money via Easypaisa</h2>
      <p>To deposit money, use the following Easypaisa number:</p>
      <div class="deposit-number">
        <strong>0312-3648826</strong>
      </div>
      <p>Follow these steps:</p>
      <ol>
        <li>Open your Easypaisa app.</li>
        <li>Go to <strong>Send Money</strong>.</li>
        <li>Enter the number <strong>0312-3648826</strong>.</li>
        <li>Enter the amount you want to deposit.</li>
        <li>Confirm the transaction.</li>
      </ol>
      <p>Share your unique referral link:</p>
      <div class="referral-link">
        <input type="text" id="referralUrl" readonly>
        <button onclick="copyReferralLink()">Copy Link</button>
      </div>
      <p>Contact us for any assistance.</p>
    </section>
  </main>
  <footer>
    <p>&copy; 2025 Ak Money. All rights reserved.</p>
  </footer>

  <script>
    function generateReferralCode() {
      const chars = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';
      let code = '';
      for (let i = 0; i < 8; i++) {
        code += chars.charAt(Math.floor(Math.random() * chars.length));
      }
      return code;
    }

    const referralCode = generateReferralCode();
    const referralUrl = `https://www.cccooo.in/?spread=${referralCode}`;
    document.getElementById('referralUrl').value = referralUrl;

    function copyReferralLink() {
      const copyText = document.getElementById('referralUrl');
      copyText.select();
      navigator.clipboard.writeText(copyText.value)
        .then(() => alert('Copied to clipboard: ' + copyText.value))
        .catch(err => alert('Failed to copy: ' + err));
    }
  </script>
</body>
</html>
/* General Styles */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.6;
  background: #f4f4f9;
  color: #333;
}

/* Header */
header {
  background: #007bff;
  color: #fff;
  text-align: center;
  padding: 20px;
}

header h1 {
  margin: 0;
  font-size: 2rem;
}

header p {
  margin: 10px 0 0;
}

/* Main Content */
main {
  padding: 20px;
}

.deposit-section {
  background: #fff;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  max-width: 600px;
  margin: 20px auto;
}

.deposit-number {
  background: #007bff;
  color: #fff;
  padding: 10px;
  font-size: 1.2rem;
  text-align: center;
  border-radius: 4px;
  margin: 10px 0;
}

ol {
  margin: 10px 0;
  padding-left: 20px;
}

.referral-link {
  margin-top: 20px;
  display: flex;
  gap: 10px;
}

input[type="text"] {
  flex: 1;
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  padding: 10px;
  border: none;
  background: #007bff;
  color: #fff;
  cursor: pointer;
  border-radius: 4px;
}

button:hover {
  background: #0056b3;
}

/* Footer */
footer {
  text-align: center;
  padding: 10px;
  background: #333;
  color: #fff;
  margin-top: 20px;
}
