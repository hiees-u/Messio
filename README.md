🔵 MESSIO
Unified Messaging Platform for Modern Businesses
1. What is Messio?

Messio is a unified messaging platform that helps businesses manage customer conversations from multiple messaging channels in one centralized inbox.

With Messio, businesses can connect multiple social pages and messaging accounts (such as Facebook Pages, Zalo OA, and more) into a single web application to receive, respond, and manage messages in real time, without any technical setup.

No app creation.
No tokens.
No webhooks.
Messio handles everything.

2. Problem Statement
Before Messio

Businesses manage multiple fanpages and messaging accounts

Messages are scattered across different platforms

High risk of missed or delayed responses

Difficult to collaborate within teams

No unified conversation history

With Messio

All messages in one inbox

Faster response times

Better team collaboration

Full conversation history per customer

Professional customer experience

3. Target Users

Messio is designed for:

Online shop owners

Small and medium-sized businesses

Game and digital service shops

Customer support teams

Sales teams handling multiple channels

No technical knowledge is required.

4. Core Features
🔐 1. Easy Channel Connection

Log in with social accounts

Select pages/accounts to connect

Messio automatically:

Retrieves access tokens

Subscribes webhooks

Handles platform configuration

📥 2. Unified Inbox

All incoming messages from all channels in one place

Clear labeling by channel and page

Unread/read status tracking

💬 3. Real-time Messaging

Send and receive messages instantly

No page refresh required

WebSocket-based real-time updates

👥 4. Conversation & Customer Management

Messages grouped by customer

Full conversation history

Easy customer identification across channels

🧑‍🤝‍🧑 5. Team Collaboration

Multiple team members per workspace

Role-based access control

Prevent duplicate replies

5. User Experience Flow (High Level)
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
Messages start flowing into unified inbox


⏱ Average setup time: under 2 minutes

6. SYSTEM FLOW DIAGRAMS
🔹 Flow 1: Authentication & Page Connection
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

🔹 Flow 2: Incoming Message (Webhook)
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
[WebSocket Emit]
      |
      v
[Unified Inbox UI]

🔹 Flow 3: Replying to a Message
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

🔹 Flow 4: Realtime Messaging
New message event
      |
      v
[Backend]
      |
      v
[Socket.IO / WebSocket]
      |
      v
[All Active Clients]

🔹 Flow 5: Token Expiry & Reconnect
Facebook API call fails
      |
      v
[Token Expired]
      |
      v
[Mark Page as "Needs Reconnect"]
      |
      v
[UI Notification]
      |
      v
[User Reconnects Channel]

7. Security & Compliance

Messio:

Uses only required permissions

Never sends automated or spam messages

Allows users to disconnect channels at any time

Does not access data beyond user authorization

Compliant with:

Facebook Platform Policy

Data privacy best practices

8. Technical Architecture Overview
[Frontend (Web App)]
        |
        v
[API Gateway]
        |
   ┌────┴─────────┐
   v              v
[OAuth Service] [Webhook Service]
   |              |
   v              v
[Facebook API]  [Message Processor]
                    |
                    v
               [Database]
                    |
                    v
               [Realtime Socket]

9. Scalability & Future Expansion

Messio is built with scalability in mind:

Multi-tenant architecture

Async webhook processing

Queue-based message delivery

Easy addition of new channels (Zalo, WhatsApp, Instagram)

10. Roadmap
Phase 1 – MVP

Facebook Pages integration

Unified inbox

Real-time messaging

Phase 2

Zalo OA integration

Advanced team roles

Conversation tagging

Phase 3

Automation rules

Analytics & reporting

AI-assisted replies

11. Brand Message

Messio — All Your Messages. One Inbox.

12. One-liner (for App Review / Pitch)

Messio is a unified messaging platform that allows businesses to connect and manage customer conversations from multiple messaging channels in one centralized inbox, with real-time communication and no technical setup required.
