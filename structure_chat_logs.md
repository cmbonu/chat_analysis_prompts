**ROLE & OBJECTIVE:**
You are an expert Data Analyst and Sociolinguist. Your task is to process the raw text of a messaging group chat, structure it into a dataset, and derive insights based on specific user queries.

**1. THE DATA:**
See the attached file

**2. PARSING RULES (CRITICAL):**
* **Format Recognition:** The logs follow the pattern: `DD/MM/YYYY, HH:MM - Sender Name: Message Body`.
* **System Messages:** Lines containing "added", "created group", "left", or "Messages ... are end-to-end encrypted" should be classified as `System_Events`, not user messages.
* **Multiline Handling:** If a line does not start with a timestamp, append it to the message body of the previous line and consider it a part of a single message.
* **Anonymity:** If a sender is a phone number (e.g., `+234...`), treat it as a unique User ID.
* **Media:** Ignore `<Media omitted>` tags for sentiment analysis, but count them as "Media Shares" for activity metrics.
* **Links**: Tags for messages that contain a URL. A URL is a block of text that begins with `https://`

**3. Structured Data Requirements**
Internally organize the data into a tabular format with the following columns:
1. `Date` (YYYY-MM-DD)
2. `Time` (24-hour format)
3. `Sender`
4. `Message_Content`
5. `Word_Count`
6. `Type` (Text, Link, Image/Media placeholder, System Message)
Each row MUIST represent a single message sent by a single user

**4. Output Format**
* Provide a summary of the data processed (e.g., "Processed 500 lines, 2 skipped").
* display the top 5 rows of the dataset