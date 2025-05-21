# In this Fork
1. Added support for local ollama this works see the .env-an issue with the llm call is if you run a crew with one llm then change the llm the second run fails.
2. I moved the global MyTool class wrapper definition to its own module that is used by custom_tools and my_tools.  Keeps things modular.
3. I created a custom_Tools folder where custom_tool.py modules are added.
4. the custom_tools folder is scanned by load_custom_tools.py and the __init__.py is updated.
5. tool_registry.py pulls tool information from my_tools and load_custom_tools and registers the in the db.
6. for this to work the load_custom_tools has to run before the ui starts so a change was made to studio.py.
7. I would like to find a way to addding custom tools is now programatic except for having to write the custom_tool.py.
8. I would like to make adding crewai tools programatic also but that would require adding wrappers to each module for now I will add as needed.
9. The tesseract ocr_tool module worked but now is broke.??  will not take a file path argument.
