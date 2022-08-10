Reduce nesting if's by negating guard clauses

```
function saveRecord(record) {
  if(record != null) {
    console.log("validate");
    
    if(record.isValid()) {
      console.log("save");
      record.save();
    }
  }
}

```
After negation, no nesting.

```
function saveRecord(record) {
  if(record == null) return;
  console.log("validate");
  
  if(!record.isValid()) return;
  console.log("save");
  record.save();
}
```
