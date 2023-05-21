# Android System Design: HLD of Chat Application


## Here are the key components required to create a robust chat application:

🔄 **Services**: Responsible for establishing and maintaining a TCP 
connection, as well as executing scheduled tasks.
🔗 **TCP Connection**: Enables real-time chat functionality using protocols like XMPP, WebSockets, or MQTT.
⏰ **Job Scheduler**: Performs periodic tasks like chat backups and data synchronization.
📩 **Push Notifications**: The backend sends notifications to users when they are offline, keeping them informed about any activity in their network.
📨 **Message Queue**: Manages outgoing and incoming messages by maintaining an organized queue.
🔄 **Transformers**: Poll messages for queue, Facilitate data transformation for incoming messages, such as mapping POJO classes or database-specific entities and for Outgoing messages.
🗄️ **Database (DB)**: Stores all chats, media links etc. in an encrypted format.
💾 **Storage**: Can store auth token and user preferences.
📁 **File Storage**: It securely stores various types of files, such as audio and video, supported by the app.
🗃️ **Repository**: Interacts with the storage manager, file manager Http calls, holds data for a single session.
📋 **Use Cases**: Defines specific actions, such as retrieving the count of unread messages.
🖥️ **View Model (VM)**: Represents the UI state and fetches relevant data based on user actions, allowing real-time updates through observers.
