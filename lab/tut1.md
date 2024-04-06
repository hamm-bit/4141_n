### LAB 1

> Computation is nothing more than checking set membership

### Q1
Before all of this, we first classify the tokens
Inputs:
    - Object in front   => @O
    - Moving foward     => @F
    - Turning           => @T

| Inputs    | Outputs   |
| --------- | --------- |
| @O        | $F1       |
| @F        | $L90      |
| @T        | $R90      |


``` psudocode
# attempt 1
# fundamental logic
# move forward until object in front
# we will then turn left

# > [!WARNING]
# > the above logic is flawed, since it can get stuck in a 2x1 box

# apart from using the "left hand on the wall" strategy,
# we have to ensure that we do not get stuck, and take all
# exist as soon as possible.
# so we develop the following logic

loop:
    $L90
    if (!@O)
        $F1
    else
        $R90
        if (!@O)
            $F1
            else
                $R90
                if (!@O)
                    $F1
                else
                    $R90
                    $F1

```


### Q2

construct a similar table to the above
| Input     | Output    |
| --------- | --------- |
| @10       | $Coke     |
| @20       | $Coffee   |
| @50       |           |
| @Coke     |           |
| @Coffee   |           |

we can build a trivial condition checker for `bal`
if `bal <= 15 - x` for x being one of 10, 20, 50 cents,
else bal will be set to `MAX = 15`

then we check if either coke or coffee is selected, then
set a roof accordingly (10 or 15)
after dispensing, set balance to 0


A successful computation should follow the safety and liveness properties set by the machines.
In this case:
> Safety: A machine should never expend coke or coffee if the amount was never reached; it should not hold balance higher than $1.50; regardless of the balance, after expending the desired drink it should reset to 0; the customers cannot change their option after the amount for the drink is reached.
> Liveness: Eventually when the machine has reached the balance, the corresponding desired drink should be released.

In fact iii) can be checked formally by looking at the limit points of the sequnece. The unexpected successful computation would be the sequence reaching a limit point that is not the infinity limit of the sequence.


### Q3
    Reject 2 of 2^3 throws


### Q4
    HW
