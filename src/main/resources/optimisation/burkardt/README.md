# burkardt

Small LP instances in MPS format from John Burkardt's dataset collection
at Florida State University. These are simple examples useful for
validating MPS parsers and basic LP solver functionality.

## Source

| | |
|---|---|
| Downloaded From | people.sc.fsu.edu/~jburkardt/datasets/mps/mps.html |
| Instances | 7 |

Several of these problems (adlittle, afiro) originate from the NETLIB
collection. The `empstest` instance is a minimal file for testing MPS
format readers.

## Models

| Name | Rows | Cols | Nonzeros |
|------|-----:|-----:|---------:|
| adlittle | 57 | 97 | 254 |
| afiro | 28 | 32 | 46 |
| empstest | 7 | 8 | 8 |
| maros | 4 | 4 | 14 |
| maros_corrected | 4 | 4 | 14 |
| nazareth | 3 | 3 | 7 |
| testprob | 4 | 3 | 6 |

Known optimal solutions (`.results` files) are available for `adlittle` and `afiro`.
