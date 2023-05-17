**&larr; [Back to Project 1 README](../README.md)**
# REST API Reference Design

This sections provides a reference design for the RESTful API for the Estate Agent system. This is an unoptimized design and can be improved.

---

## Schemas

<pre>
<b>action</b> {
    date : time
    action : string
    command : string
    status : string
}
</pre>

<mark>Note</mark>: status can be SUCCESS or FAILED

---

## Backup Remote Folder

>**GET** /backup/{folder_name} e.g. http://localhost:8080/backup/mypictures
>
><b>Parameters:</b> no parameters

><b>Request Body</b> N/A

>**Response:** 201 CREATED

## Display Logs

>**GET** /log e.g. http://localhost:8080/logs?{start-date}&{end-date}
>
>**Parameters:**  
>- start-date: date for the fist record in the set to be returned in datetime format  
>- end-date: date for the last record in the set to be returned in datetime format  

>**Response** 200 OK
<pre>
<b>[ action{...} ]</b>

<b>Example</b>
[
    {
        "date" : "2024-12-06T15:00:00Z",
        "action" : "TBA",
        "command" : "TBD",
        "status" : "SUCCESS"
    },
    {
        "date" : "2024-12-07T16:00:00Z",
        "action" : "TBA",
        "command" : "TBD",
        "status" : "FAILED"
    }
]
</pre>

