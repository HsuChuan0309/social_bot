<!DOCTYPE html>
<html lang="zh-TW">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Chatbot</title>

<script src="https://www.gstatic.com/dialogflow-console/fast/messenger/bootstrap.js?v=1"></script>

<style>
  body, html {
    margin: 0;
    padding: 0;
    height: 100%;
  }
  df-messenger {
    --df-messenger-bot-message: #f1f1f1;
    --df-messenger-user-message: #fce9ff;
    --df-messenger-font-color: black;
    --df-messenger-chat-background-color: white;
    width: 100%;
    height: 100%;
  }
</style>
</head>
<body>

<df-messenger
  intent="WELCOME"
  chat-title="0806"
  agent-id="236034eb-ea4a-47e7-b0c8-202f144d704e"
  language-code="zh-tw">
</df-messenger>

<script>
  // 例：當偵測到對話完成時，通知父頁面 (Qualtrics) 顯示下一頁按鈕
  window.addEventListener("message", (event) => {
    if (event.data === "chat-finished") {
      window.parent.postMessage("show-next-button", "*");
    }
  });
</script>

</body>
</html>
