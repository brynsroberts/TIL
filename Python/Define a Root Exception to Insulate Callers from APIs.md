- Defining root exceptions for modules allows API consumers to
insulate themselves from an API.
- Catching root exceptions can help you find bugs in code that
consumes an API.
- Catching the Python Exception base class can help you find bugs in
API implementations.
- Intermediate root exceptions let you add more specific types of
exceptions in the future without breaking your API consumers.