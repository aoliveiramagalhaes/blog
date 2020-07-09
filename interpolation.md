## how to add a string interpolation

**Example 1**

```javascript

const reportingForDuty = (rank, lastName) => {
  return `${rank} ${lastName} reporting for duty!`
}

console.log(reportingForDuty('Private', 'Fido')) // Should return 'Private Fido reporting for duty!'
console.log(reportingForDuty('Major', 'Diaz')) // Should return 'Major Diaz reporting for duty!'

```

**Example 2**

```javascript

const sillySentence = (adjective, verb, noun) => {
  return `I am so ${adjective} because I ${verb} coding! Time to write some more awesome ${noun}!`
}

console.log(sillySentence('excited', 'love', 'functions')) 
// Should return 'I am so excited because I love coding! Time to write some more awesome functions!'

```

**Note**

The corect character is ` (backtick). Do not use ' or '' (quotation marks).
