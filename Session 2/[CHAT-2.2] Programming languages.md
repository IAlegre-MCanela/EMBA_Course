# [CHAT-2.2] Programming languages

## Input

Write a Python function to check whether a given integer is prime, discussing, in no more than 50 words, the logic on which your code is based.

Apply the function to a few examples. 

## Output (Gemma 3 4B)

```
python

def is_prime(n):
  """Checks if an integer n is prime."""
  if n <= 1: return False
  for i in range(2, int(n**0.5) + 1):
    if n % i == 0: return False
  return True

# Examples
print(is_prime(2))   # True
print(is_prime(10))  # False
print(is_prime(17))  # True
```

**Logic:** The function iterates from 2 up to the square root of `n`. If any number within this range divides `n` evenly, it's not prime. Otherwise, it is. This optimization avoids unnecessary checks.

---

## Input

Write a Java function to check whether a given integer is prime, discussing, in no more than 50 words, the logic on which your code is based.

Apply the function to a few examples. 

## Output (Gemma 3 4B)

```
java

class Solution {
    public boolean isPrime(int n) {
        if (n <= 1) return false;
        for (int i = 2; i * i <= n; i++) {
            if (n % i == 0) return false;
        }
        return true;
    }

    public static void main(String[] args) {
        Solution sol = new Solution();
        System.out.println(sol.isPrime(2)); // True
        System.out.println(sol.isPrime(10)); // False
        System.out.println(sol.isPrime(17)); // True
    }
}
```

**Logic:** The code iterates from 2 up to the square root of `n`. If any number divides `n` evenly, it's not prime.  This optimization avoids unnecessary checks because if a number has a divisor greater than its square root, it must also have a divisor smaller than its square root.