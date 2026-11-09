ENDEMIS / FluidFlux water reference bundle
Expected project: G:\Projects\TEST
Expected content: G:\Projects\TEST\Content\FluidFlux
Expected map file: G:\Projects\TEST\Content\FluidFlux\Demo\Maps\FluxCoastlineMap.umap
Expected map package: /Game/FluidFlux/Demo/Maps/FluxCoastlineMap

Reference materials and Niagara exports are for analysis only: recreate these assets in ENDEMIS. Only texture and sound assets are eligible for direct reuse.
exports/PIEProbe/ requires an active PIE world. If no fresh probe JSON exists, runtime state was not captured and no runtime acceptance is claimed.
exports/ReferenceValues/ contains the existing explicit-list material, Blueprint, texture, collection and level-actor dump.
exports/RuntimeValues/ contains the existing level-actor MID dump.
exports/WaterLogic/ contains T3D, graph and HLSL exports from both configured water roots and the bounded supported dependency closure.
The existing Saved/ENDEMISExport/Water folder is restored after extraction.

SIZE AND RESTORE POLICY
Every bundle file is at most 80 MiB. Larger fresh exports are stored as numbered binary parts under file_parts/; segment-index-*.jsonl records the job name, Saved output root, job-relative source path, part number/count, zero-based byte offset, byte size, part SHA-256, and complete source size/SHA-256. To restore a source, select segment_index_files from its manifest job, collect that source's part records, sort by part_number, verify each part hash and contiguous offset, concatenate part_relative_path files, then verify source_size_bytes and source_sha256. The helper _reassemble_segmented_file performs these checks and writes the restored file atomically.
All bundle files are stored in one ordinary ZIP archive named in manifest.json. The archive is not split and may exceed 90,000,000 bytes; individual bundle files remain within the 80 MiB limit and large source files use the lossless parts/index scheme above.

Missing values, getter errors, protected UE properties and truncation are described in the reports; a missing value is not a confirmed zero. Project assets are not modified.
