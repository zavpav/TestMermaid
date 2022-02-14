Test mermaid

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```


```mermaid
sequenceDiagram
    Alice->>Bob: Hello Bob, how are you?
    alt is sick
        Bob->>Alice: Not so good :(
    else is well
        Bob->>Alice: Feeling fresh like a daisy
    end
    opt Extra response
        Bob->>Alice: Thanks for asking
    end
```

```mermaid
sequenceDiagram
participant "A service" as srv
participant "MainBot" as mb
participant "Telegram\nservice" as tg
actor "User" as usr

usr -> tg : Request infromation
tg -> mb : Request information by user
mb -> mb : Identify type of infromation
mb -> mb : Find internal message id for this request
mb -> tg : Delete internal MessageId for this user
mb -> srv : Request infromation
mb <-- srv: Response information
mb -> mb : Generate telegram messages
mb -> tg : Send messages 
tg -> usr: Send new messages\n[because message id was deleted]
```



# TestMermaid