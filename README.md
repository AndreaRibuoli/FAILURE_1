# FAILURE_1

When installed with PASERIE/INSTALL will fail because of missing **GUIDANCE.TXT**

```
PASERIE/INSTALL GIT_USER(AndreaRibuoli) PACKAGEN(FAILURE_1)
```

The problem can be identified using the option `VERBOSE('Y')`:

```
PASERIE/INSTALL GIT_USER(AndreaRibuoli) PACKAGEN(FAILURE_1) VERBOSE('Y')
```

A spool file will log the HTTP/1.1 error **404 Not Found**:

```
                             Display Spooled File                             
File  . . . . . :   QPRINT                           Page/Line   1/22         
Control . . . . .                                    Columns     1 - 78       
Find  . . . . . .                                                             
*...+....1....+....2....+....3....+....4....+....5....+....6....+....7....+...
> GET /repos/AndreaRibuoli/FAILURE_1/contents/GUIDANCE.TXT HTTP/1.1           
Host: api.github.com                                                          
User-Agent: curl/0007.0073.0000                                               
Accept: application/vnd.github.v3.raw                                         
Authorization: token d4dbeefc47e11a29299017971d629894cea2f2b3                 
* old SSL session ID is stale, removing                                       
* Mark bundle as not supporting multiuse                                      
< HTTP/1.1 404 Not Found                                                      
```
