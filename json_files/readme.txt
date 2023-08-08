This is a document of the "TEST" applications. In this application, there are 3 types of blocks
which are instrument-connection, if-else and repeat blocks.

Below describes when we should use them.
When the user wants to connect to an instrument, he should use the "instrument-connection" block.
The json of it looks like this:
```
{
    "type": "instrument-connection",
    "ApplicationID": "",
    "Address": "",
    "ModelNumber": "",
    "PropertyID": "",
    "value": ""
},
```

when the user wants to have an if else statement like in the programming. They should use the "if-else" block
like this:
```
{
    "type": "if-else",
    "condition": 
    [
        {
        
        }
    ],
    "if-branch":
    [
        { }
    ],
    "else-branch":
    [
        { }
    ]
},
```
when the user wants to have loop statement like in the programming such as while loop. They should use the "repeat" block
like this:
{
    "type":"repeat",
    "condition": 
    [
        {
        
        }
    ],
    "execution":[]
}

These blocks are meant to be placed/used step by step.
For example, there is a scenario that the user wants to connect to an instrument of model "ABCD" in a loop.
they would use the json blocks like this:

{
    "type":"repeat",
    "condition": 
    [
        {
            "value": "1 == 1"
        }
    ],
    "execution":[
        {
            "type": "instrument-connection",
            "ApplicationID": "",
            "Address": "",
            "ModelNumber": "ABCD",
            "PropertyID": "",
            "value": ""
        }
    ]
}