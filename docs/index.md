# Introduction

<figure><img src="/sayanchat.png" alt=""><figcaption></figcaption></figure>

<figure markdown="span">
  ![Image title](https://raw.githubusercontent.com/Mohamad82Bz/sayanchat-docs/refs/heads/master/sayanchat.png)
</figure>

Welcome to the **SayanChat** documentation. SayanChat is a Minecraft: Java Edition spigot/paper plugin designed to enhance the chat experience on your server. It provides variety of features to manage and customize chat interactions, ensuring a seamless and rich chat experience for players.

## Key Features

### Chat Boxes

SayanChat's standout feature is its versatile **chat boxes**. Players can seamlessly switch between various chat types, including the server-wide **global chat**, **private chats**, and **custom chat boxes** like permission-based ones (e.g., a dedicated staff chat). This functionality helps create a cleaner, more organized chat experience while reducing unwanted spam.

For instance, a player can open a **private chat box** with a friend, isolating their conversation from all other messages. While in this private chat box, they won’t see messages from other players. Upon exiting the private chat, they’ll return to the **global chat** and regain access to its message history.

### Feature Packed

* **Synchronized Chat**: SayanChat allows multiple servers to share the same chat, enabling **network-wide chat boxes**. This is particularly useful for features like staff chats and notifications for staff regarding swearing or advertising.
* **Chat History**: SayanChat includes a **Chat History** feature that saves all player and system messages to the database. This ensures a seamless chat experience by providing access to past messages when switching between chat boxes or rejoining the server.\
  Admins can also retrieve chat history using a dedicated command, making it easier to review conversations and manage server interactions.
* **Default Colors**: Players can set a **default message color**, ensuring all their messages are automatically displayed in their chosen color.
* **Nicknames**: Players can create **network-wide nicknames** with colors and formatting for personalization.
* **Announcements**: Supports both **manual** and **automated network-wide messages**, keeping players informed with ease.
* **Compatibility**: Designed to work seamlessly alongside other plugins that interact with chat.
* **Configurable**: Every aspect of SayanChat, from chat box settings and rules to announcements and default colors, is fully customizable.
* **Database Options**:
    * SayanChat supports **SQLite**, **MySQL**, and **MariaDB** for database connectivity.
    * **SQLite** is the default option and works out of the box with no additional configuration.

!!! tip
    To fully utilize features like synchronized chat boxes (e.g., private messages across servers), a **MySQL** or **MariaDB** database is required.
