# optimisation-models

Collection of optimisation test models (LP/MIP/QP) packaged as classpath
resources. Used by [ojAlgo](https://github.com/optimatika/ojAlgo) and
related projects for regression testing and benchmarking.

Models with more than 10k variables or constraints, or individual files
of 100MB or more, are excluded from all collections to keep the
repository and Maven artifact manageable.

## Collections

| Collection | Models | Format | Problem Types | Source |
|:-----------|-------:|:-------|:--------------|:-------|
| [burkardt](src/main/resources/optimisation/burkardt) | 7 | MPS | LP | people.sc.fsu.edu/~jburkardt/datasets/mps/mps.html |
| [marosmeszaros](src/main/resources/optimisation/marosmeszaros) | 113 | SIF | Convex QP | ftp.numerical.rl.ac.uk/pub/cuter/marosmeszaros |
| [meszaros](src/main/resources/optimisation/meszaros) | 71 | MPS | LP | Meszaros LP test set |
| [netlib](src/main/resources/optimisation/netlib) | 97 | SIF | LP | numerical.rl.ac.uk/cute/netlib.html |
| [MIPLIB](src/main/resources/optimisation/MIPLIB) | 495 | MPS | MIP | miplib.zib.de |
| [QPLIB](src/main/resources/optimisation/QPLIB) | 382 | LP + SOL | QP / MIQP | qplib.zib.de |

### burkardt

Small LP instances from John Burkardt's MPS dataset collection.

### marosmeszaros

The Maros-Meszaros convex QP test set in SIF format. 113 instances
included (25 larger ones excluded). All problems have convex quadratic
objectives and linear constraints.
See [marosmeszaros/README.md](src/main/resources/optimisation/marosmeszaros/README.md)
for per-instance details.

### meszaros

The Meszaros LP test set. 71 linear programming instances in MPS format.

### netlib

The classic NETLIB LP test set in SIF format. 97 instances included
(17 larger ones excluded). Widely used for benchmarking LP solvers.
See [netlib/README.md](src/main/resources/optimisation/netlib/README.md)
for per-instance details.

### MIPLIB

Combined collection from all MIPLIB editions (2.0, 3.0, 2003, 2010, 2017),
filtered to easy instances with at most 10k rows and 10k columns.
495 mixed-integer programming instances in MPS format.
See [MIPLIB/README.md](src/main/resources/optimisation/MIPLIB/README.md)
for per-instance details and edition membership.

### QPLIB

382 quadratic programming instances from QPLIB in LP format with
solution files. Covers linear, convex, and non-convex objectives with
continuous, binary, integer, and mixed variables. Instances with more
than 10k variables or constraints are excluded (71 total), as is one
smaller instance whose dense quadratic objective produces a file
exceeding 100MB. See [QPLIB/README.md](src/main/resources/optimisation/QPLIB/README.md)
for per-instance details, problem type codes, and the full list
including excluded instances available from qplib.zib.de.

## Usage

Add as a test dependency:

```xml
<dependency>
    <groupId>org.ojalgo</groupId>
    <artifactId>optimisation-models</artifactId>
    <version>1.1.0-SNAPSHOT</version>
    <scope>test</scope>
</dependency>
```

Models are available on the classpath under `optimisation/{collection}/`.

## License

MIT
