# Chat

The chat page allows the User to chat with their data. The chat is scoped to the current team that is selected. The AI will use the data sources available to that team to answer the User's question.

![The chat page](/images/chat/chat_response.png)

A new chat can be created by selecting the 'Start New' button in the chat bar at the bottom of the screen. To see all chats select 'Recent' -> 'Chat History'.

To rename a chat, select the pencil icon by the chat name at the top of the chat window. Chats can also be renamed in the Chat History view. Names are given automatically based on the initial question in the chat.

![The chat history page](/images/chat/chat_history.png)

## Visualizations

The AI is able to produce visualizations in addition to data objects. The following visualization types are supported:
- Bar
- Line
- Area
- Scatter
- Pie

![Visualization example](/images/chat/viz_chat_example.png)

Visualizations are created using the Plotly open source library. 

## Auditing the AI output

After providing your prompt, the user is able to see the AI's thoughts in real-time. This helps the User understand the thought process the AI went through to reach its conclusion and helps the User audit the result. 

![Showing the AI thoughts](/images/chat/ai_thoughts.png)

The AI thoughts are not permanently saved however and when the page is reloaded won't be available. You can also see the SQL query used to generate the output by clicking 'See SQL'. 

Finally, the AI will provide a data object in response to your prompt if the prompt requires it to use a datasource.

![A dataset returned by the AI](/images/chat/chat_dataset.png)

Using the data spreadsheet view, you can download or save the data. If you decide to save the data by selecting the star icon, you will see a modal window pop-up with a title and description auto-populated by the AI. The title and description can be edited before saving. Saved data will appear in the data page that can be selected in the sidebar.

![Saving the data](/images/chat/save_data_view.png)

There are also 2 options at the bottom of the window. The user can share the data object with their team or save the results to a Collection.

### Verified Results

Users can mark a result as 'verified'. When Users mark a result as verified, it will add a checkmark to the result. 

![Verified result example](/images/chat/verified_result.png)

Verifying a result will add that result to the cache, which means it will return instantly for other users once it has been added. 

There are 2 types of semantically similar results that can be returned in the cache:
- Identical: These results will return the same information as was originally cached if it is current within the last day. If it is older than 1 day, then the result is refreshed.
- Similar: These results will return different information, but the SQL query only differs in the where clause being applied. For example, if someone asks 'how many bagels are there?' and someone else asks, 'how many sesame seed bagels are there', the 2nd query is similar enough to be verified (we know how to count bagels), but will be updated to filter to sesame seed bagels only.

Other details to be aware of:
- If a verified result is returned and is older than 1 day, the SQL query is re-ran in order get the latest information. 
- The checkmark symbol used to indicate if a result is verified is outlined if it was by a Member and solid if it was verified by an Admin
- An Admin can confirm the verification of a Member to promote that verification to an admin

Verified results is a great initial step to getting common consensus around common metrics. Every time a result is returned, users can verify the output and other members will get the same query ran for them as well.

#### Unverifying a Result

These verified results can also be unverified if another user disagrees that this information looks correct. However, a user has to be at the same RBAC role level or greater as the other user to unverify. For example, if the user is a Member, they can't unverify an Admin's verified result.

Once a result is unverified, prior verified results that were returned as verified based on that verified data object, will be unverified for anyone who received them. This ensure the highest level accuracy and agreement possible for human-verified information from the AI.

#### Security Implications

Identical verified results are only returned for users who share a database connection through their teams. Similar results are only returned for an organization if two users share the same database, but not necessarily the same connection. This is important for situations where Users rely on jinjafied schemas. The query is re-ran to get the information relevant to the other user's connection, but the query itself remains verified.

This setup ensures that only those who have access to shared connections are able to view semantically similar information and keeps the data secure.

## Double-Texting

The AI has the ability to answer questions simultaneously. Before the AI completes its response, you can ask it another question and it will start answering both questions in parallel. 

## Result Output

While chatting with the AI, you will generate results for your queries. These results have limitations however. You cannot generate a result over 100 MB. Results over 1 week old in your chat history are not saved. 

## Stopping a Chat

While the AI is thinking through a problem, you have the option to stop the chat. In order to stop the chat, select the blue square icon that shows above the up-pointing chevron in the chat toolbar. This will stop all running requests within the chat.

![Stopping the chat](/images/chat/stop_chat.png)