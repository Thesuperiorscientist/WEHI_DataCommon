# Limitations

## Chromosome 22 Only

The workflow does not represent a complete whole-genome analysis.

The initial attempt to work with the full GRCh38 reference was limited by available system memory.

Chromosome 22 was therefore selected as a computationally manageable reference.

## Consequences

Because the workflow is restricted to chromosome 22:

- Results do not represent genome-wide variation.
- Variants outside chromosome 22 are not included.
- Genome-wide coverage cannot be assessed.
- The generated VCF files should not be interpreted as complete whole-genome variant calls.

## Synthetic Data

The generated samples were intended for demonstration, training, and workflow development.

They should not be interpreted as independent biological samples or as clinical datasets.

## Computational Environment

The workflow was developed in a resource-constrained environment. Some decisions were therefore made based on available memory and network accessibility rather than computational optimality.

## Reproducibility

The technical diary preserves the original development process, including unsuccessful approaches and subsequent adaptations.