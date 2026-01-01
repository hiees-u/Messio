# Messio  
### Unified Messaging Platform for Modern Businesses

Messio is a unified messaging platform that helps businesses manage customer conversations from multiple messaging channels in one centralized inbox.

With Messio, businesses can connect multiple social pages and messaging accounts (such as Facebook Pages, Zalo OA, and more) into a single web application to receive, respond to, and manage messages in real time — without any technical setup.

> No app creation.  
> No tokens.  
> No webhooks.  
> Messio handles everything.

---

## 🚀 Features

- 🔐 **Easy Channel Connection**  
  Connect social pages and messaging accounts with a simple login and selection flow.

- 📥 **Unified Inbox**  
  Receive all messages from multiple channels in a single, organized inbox.

- 💬 **Real-time Messaging**  
  Send and receive messages instantly with live updates.

- 👥 **Conversation Management**  
  Automatically group messages by customer and maintain full conversation history.

- 🧑‍🤝‍🧑 **Team Collaboration**  
  Support multiple agents with role-based access control.

---

## 🎯 Who Is Messio For?

Messio is designed for:
- Online shop owners
- Small and medium-sized businesses
- Game and digital service providers
- Customer support and sales teams

No technical knowledge is required.

---

## 🔄 High-Level User Flow

```
User signs up
      ↓
User logs in with Facebook
            ↓
Messio retrieves available pages
               ↓
User selects pages to connect
               ↓
Messio auto-configures integration
               ↓
Messages start flowing into the unified inbox
```

---

## 🧩 System Flow Diagrams

### 1. Authentication & Page Connection

```
[User Browser]
      |
      | Click "Connect Facebook"
      v
[Facebook OAuth]
      |
      | Authorization Code
      v
[Messio Backend]
      |
      | Exchange token
      v
[Facebook Graph API]
      |
      | Pages + Page Tokens
      v
[Messio Backend]
      |
      | Auto subscribe webhook
      v
[Connected Page Active]
```

---

### 2. Incoming Message (Webhook)

```
Customer sends message
         |
         v
[Facebook Page]
      |
      v
[Facebook Webhook]
         |
         v
[Messio Webhook Receiver]
      |
      | Identify workspace & page
      | Create / match conversation
      | Store message
      v
[Database]
   |
   v
[Realtime Socket Emit]
      |
      v
[Unified Inbox UI]
```

         ---

### 3. Sending a Message

```
Agent types message
         |
         v
[Messio Web App]
      |
      v
[Messio API: Send Message]
         |
         v
[Facebook Send API]
         |
         v
[Customer Receives Reply]
            |
            v
[Message Status Updated]
```

---

### 4. Realtime Messaging

```
New message event
   |
   v
[Backend]
   |
   v
[WebSocket / Socket.IO]
         |
         v
[All Active Clients]
```
---

### 5. Token Expiry & Reconnect

```Facebook API call fails
      |
      v
[Token Expired]
      |
      v
[Page marked as NEEDS_RECONNECT]
            |
            v
[User notified in UI]
            |
            v
[User reconnects channel]
```

---

## 🔐 Security & Compliance

- Uses only required platform permissions
- Does not send automated or spam messages
- Allows users to disconnect channels at any time
- Complies with Facebook Platform Policies

---

## 🏗 Technical Architecture
```
[Frontend (Web App)]
      |
      v
[API Gateway]
      |
┌─────┴──────────┐
v                v
[OAuth Service] [Webhook Service]
   |                |
   v                v
[Facebook API] [Message Processor]
   |
   v
[Database]
   |
   v
[Realtime Socket]
```

---

## 📈 Roadmap

### Phase 1 – MVP
- Facebook Pages integration
- Unified inbox
- Real-time messaging

### Phase 2
- Zalo OA integration
- Advanced team roles
- Conversation tagging

### Phase 3
- Automation rules
- Analytics & reporting
- AI-assisted replies

---

## 🏷 Brand Message

> **Messio — All Your Messages. One Inbox.**

---

## 📌 License

MIT License

---

## 🤝 Contributing

Contributions are welcome. Please open an issue or submit a pull request.

---

## 📬 Contact

For questions or partnerships, please contact the Messio team.
