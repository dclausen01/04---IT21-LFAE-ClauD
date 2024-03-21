
``` javascript
function mergeSplit(arr) {
	if (arr.length <= 2) {
		return sorted([arr[0]], [arr[1]])	
	} else {
	return sorted(mergeSplit(arr.slice(0, arr.length/2)),
				  mergeSplit(arr.slice(arr.length/2, arr.length))
				  )
	}
}

function sorted(lArr, rArr) {
	let lpointer = 0;
	let rpointer = 0;
	
}
```