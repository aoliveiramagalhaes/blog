## how to add a string interpolation

```javascript

const reportingForDuty = (rank, lastName) => {
  return `${rank} ${lastName} reporting for duty!`
}

console.log(reportingForDuty('Private', 'Fido')) // Should return 'Private Fido reporting for duty!'
console.log(reportingForDuty('Major', 'Diaz')) // Should return 'Major Diaz reporting for duty!'

```
**Note**

The corect character is ` (backtick). Do not use ' or '' (quotation marks).
