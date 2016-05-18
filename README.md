log
===

Extension module of golang logging

Default output to stderr

redirect to a file:

```
Logfile="test.log"

f, err := os.OpenFile(Logfile, os.O_APPEND|os.O_CREATE|os.O_WRONLY, 0644)
if err != nil {
        log.Fatal("can not open file")
}
log.Info("Redirect log to file: ", Logfile)
log.Std = log.New(f, "", log.Ldefault)
```
