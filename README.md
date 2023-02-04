1. Create a C# web application
2. Expose endpoint that will request a code(only one); When a user requests code, check if a un-used code is available in-memory if it is send it in the response and mark it as used. If there were no un-used codes then make a call to retrieve 500 codes(treat codes as UUID's please look at https://www.uuidgenerator.net/api) and keep them in memory and send one back. Should we maintain used codes in memory?
4. Handle case where multiple users requests a code, and you don't have any un-used ones in memory. Achieve some concurrency here, and prevent multiple calls to UUID generator.
5. Try to add test cases. But not mandatory.
6. Try to work on weekdays(5 AM - 10 AM), so that you will know if you can handle both.
