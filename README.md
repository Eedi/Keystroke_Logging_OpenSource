# Keystroke_Logging_OpenSource
a keystroke logging mechanism to collect keystroke data for R&amp;D purposes

The keystroke logging mechanism unobtrusively collects information about users' keystroke and mouse operations from the front end using a keystroke logging program written in JavaScript. The information is aggregated and posted to the back end whenever the user hits the "Send" button in the chatbot. At the back end, the keystroke information is handled via a FastAPI app that connects to a cloud-based Azure table storage. Finally, all the keystroke information is stored in the Azure table storage in tabular format.

In the output of keystroke data, Event ID indexes the keyboard and mouse operations in chronological order. EventTime denotes the time (in milliseconds) when a key or the mouse was pressed. Output shows the content of the keystroke or mouse event. CursorPosition registers cursor position information to help keep track of the location of the leading edge. Additionally, TextChange shows the exact changes made to the current text while Activity indicates the nature of the changes (e.g., Input, Remove/Cut).  

