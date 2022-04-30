# ExpenseRemoved
When an expense is deleted from the database. Attachments are also deleted, thus we share again the list of upload ids so you can synchronize easier.

## Example

```
{
   "expenseId":"4ff2f988-7c0a-424f-b988-45d6b9f8c6d4",
   "uploadIds":[
      "6260f93eb6fe2120e0d8d960"
   ],
   "version":"V1",
   "timestamp":1651319378888,
   "eventName":"ExpenseRemoved"
}
```