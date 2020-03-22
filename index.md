# FLUID: A Common Model for Semantic Structural Graph Summaries based on Equivalence Relations

FLUID (short for: FLexible graph sUmmarIes for Data graphs) is a mathematical model based on equivalence relations to define __structural graph summaries__ [1,3]. Structural graph summaries are a condensed representation of graph such that the vertices are partitioned based on equivalent sub-graphs, e.g., using _k_-bisimulation.
Structural graph summaries are usually a magnitude smaller than the input graph, but a set of predefined (structural) features are equivalent to the original graph.
Thus, they are used as indices in various applications.
These indices are sometimes referred to as __schema-level indices__.

In the FLUID project, we implemented the basic building blocks, i.e., the Schema Elements along with their parameterizations in a generic, modular processing pipeline. This enables users to easily configure and compute any schema-level index.
Furthermore, the framework comes with a generic FLUID query engine that is able to perform structural queries on any index modeled with FLUID.

### References

1. Blume, T., Scherp, A.: Towards flexible indices for distributed graph data: The formal schema-level index model FLuID. In: 30th GI-Workshop on Foundations of Databases (Grundlagen von Datenbanken). CEUR Workshop Proceedings (2018), http://ceur-ws.org/Vol-2126/paper3.pdf.
2. Konrath, M., Gottron, T., Staab, S., Scherp, A.: SchemEX - efficient construction of a data catalogue by stream-based indexing of Linked Data. J. Web Sem. 16, 52–58 (2012)
3. Blume, T., Scherp, A.: FLuID: A Meta Model to Flexibly Define Schema-level Indices for the Web of Data. CoRR abs/1908.01528 (2019)

### Acknowledgments
This research was co-financed by the EU H2020 project [MOVING](http://www.moving-project.eu/) under contract no 693092.
