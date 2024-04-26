# CGN-Extention (Compressed Game Notation Browser Extension)

CGN-Extension is a simple browser extension for the CGN (Compressed Game Notation) library I created. It allows you to compress and decompress PGN files using the CGN library. It is designed to be fast, efficient, and flexible. It supports WASM compilation via wasm-pack, and contains 4 different compression algorithms to choose from.

By default, the extension uses the `opening-huffman` algorithm, which is the most efficient algorithm for compressing PGN data. 

## Algorithms (High to Low Compression Ratios --- Low to High Speed)
1) `opening-huffman` - A Huffman encoding algorithm that uses the huffman-encoding crate to compress the PGN data, but with an additional optimization for compressing common opening moves. 
2) `dynamic-huffman` - A Huffman encoding algorithm that uses the huffman-encoding crate to compress the PGN data, but with a huffman tree that is updated dynamically as the data is compressed.
3) `huffman` - A Huffman encoding algorithm that uses a huffman-encoding crate to compress the PGN data.
4) `bincode` - A simple binary encoding algorithm that uses the bincode crate to serialize the PGN data into a binary format.

## Installation
1) Open your browser and navigate to "chrome://extensions/" (assuming you are using Chrome).
2) Enable "Developer mode" in the top right corner.
3) Click "Load unpacked" and select this /cgn-cli directory
4) The extension should now be installed and ready to use.