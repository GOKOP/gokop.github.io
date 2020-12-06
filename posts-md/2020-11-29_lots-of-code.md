# Lots of code

Cause why not

## Rust
```rust
// Print the binomial coefficient table, first 10 rows

fn main() {
	for n in 0..11 {

		let mut val: i32 = 1;
        for k in 0..n+1 {

            if n != 0 && k != 0 {
                val = val * (n+1-k) / k;
            }

            print!("{}\t", val);
        }
        print!("\n");
	}
}
```

## C
```c
#include <stdio.h>

// Print the binomial coefficient table, first 10 rows

int main() {
	for(int n=0; n<=10; ++n) {

		int val = 1;
		for(int k=0; k<=n; ++k) {

			if(n != 0 && k != 0) {
				val = val * (n+1-k) / k;
			}

			printf("%i\t", val);
		}
		printf("\n");
	}

	return 0;
}
```

## Go
```go
import "fmt"

// Print the binomial coefficient table, first 10 rows

func main() {
	for n := 0; n<=10; n++ {

		val := 1
		for k := 0; k<=n; k++ {

			if n != 0 && k != 0 {
				val = val * (n+1-k) / k
			}

			fmt.Print(val, "\t")
		}
		fmt.Print("\n")
	}
}
```

## PHP
```php
<?php

// Print binomial coefficient table, first 10 rows

for($n=0; $n<=10; $n++) {

	$val = 1;
	for($k=0; $k<=$n; $k++) {
		
		if($n != 0 && $k != 0) {
			$val = $val * ($n+1-$k) / $k;
		}

		echo "$val\t";
	}
	echo "\n";
}
?>
```

## Python
```python
# Print binomial coefficient table, first 10 rows

for n in range(11):

    val = 1
    for k in range(n+1):
        
        if n != 0 and k != 0:
            val = val * (n+1-k) / k

        print(val, end="\t")

    print("")
```

## POSIX shell
```sh
# just don't

alias echo="/bin/echo" # guarantees consistent echo behavior

for n in $(seq 10); do

	val=1
	for k in $(seq $n); do
		
		if [ $n != 0 ] && [ $k != 0 ]; then
			val=$(echo "$val * ($n+1-$k) / $k" | bc)
		fi

		echo -ne "$val\t"
	done
	echo ""
done
```
