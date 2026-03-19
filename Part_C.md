Q1 — What is NumPy broadcasting? Why is it useful?
>
Broadcasting allows NumPy to perform operations on arrays of different shapes by automatically expanding smaller arrays to match larger ones without copying data.
Useful because:
Eliminates loops
Faster computation
Cleaner code

Q2 (Coding) — Implement: normalize(X)
● Scale values between 0 and 1 using NumPy
> 
def normalize(X):
    return (X - np.min(X)) / (np.max(X) - np.min(X))
X = np.array([5, 10, 15])
print(normalize(X))

Q3 — What is the difference between vectorisation and loops? Why is NumPy faster?
>
Aspect	            Vectorisation	Loops
Execution	        C-level (fast)	Python-level (slow)
Readability     	Clean	        Verbose
Performance	        High	        Low
Memory	            Efficient	    Less efficient
Why NumPy is faster:
Uses compiled C backend
Avoids interpreter overhead
Uses parallel CPU instructions