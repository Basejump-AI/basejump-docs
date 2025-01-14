# Chat

The chat page allows the User to chat with their data. The chat is scoped to the current team that is selected. The AI will use the data sources available to that team to answer the User's question.

![The chat page](/images/chat/chat_response.png)

A new chat can be created by selecting the 'Start New' button in the chat bar at the bottom of the screen. To see all chats select 'Recent' -> 'Chat History'.

To rename a chat, select the pencil icon by the chat name at the top of the chat window. Chats can also be renamed in the Chat History view. Names are given automatically based on the initial question in the chat.

![The chat history page](/images/chat/chat_history.png)

## Auditing the AI output

After providing your prompt, the user is able to see the AI's thoughts in real-time. This helps the User understand the thought process the AI went through to reach its conclusion and helps the User audit the result. 

![Showing the AI thoughts](/images/chat/ai_thoughts.png)

The AI thoughts are not permanently saved however and when the page is reloaded won't be available. You can also see the SQL query used to generate the output by clicking 'See SQL'. 

Finally, the AI will provide a data object in response to your prompt if the prompt requires it to use a datasource.

![Showing the AI thoughts](/images/chat/chat_dataset.png)

Using the data spreadsheet view, you can download or save the data. If you decide to save the data by selecting the star icon, you will see a modal window pop-up with a title and description auto-populated by the AI. The title and description can be edited before saving. Saved data will appear in the data page that can be selected in the sidebar.

![Saving the data](/images/chat/save_data_view.png)

There are also 2 options at the bottom of the window. The user can share the data object with their team or save the results to a Collection.

## Double-Texting

The AI has the ability to answer questions simultaneously. Before the AI completes its response, you can ask it another question and it will start answering both questions in parallel. 