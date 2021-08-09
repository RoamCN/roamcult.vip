
# Backlinks
## [August 9th, 2021](August 9th, 2021.md)
- [Weekly Summary](Weekly Summary.md)

## [Day Log](Day Log.md)
const results={};timeEntries.forEach((entry)=>{const logMatch=entry.match(/^(\d+:\d+) - (\d+:\d+) (.*?):/);if(logMatch){const timeDiff=moment(logMatch[2],"HH:mm").diff(moment(logMatch[1],"HH:mm"),"minutes");const key=logMatch[3].trim();const existingTime=results[titleForKey[key]||key]??0;results[titleForKey[key]||key]=existingTime+timeDiff;}});console.log(results);const toPrint=[`[Weekly Summary](Weekly Summary.md)

