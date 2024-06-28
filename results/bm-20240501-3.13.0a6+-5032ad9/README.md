# Results

- fork: faster-cpython
- version: 3.13.0a6+
- config: 
- commit hash: [5032ad9](https://github.com/faster%2dcpython/cpython/commit/5032ad9)
- commit date: 2024-05-01T14:56:12+01:00
- commit merge base: [21c09d9f8195433f34b72ddfa25dd1bda3019ed7](https://github.com/faster%2dcpython/cpython/commit/21c09d9f8195433f34b72ddfa25dd1bda3019ed7)
- ref: use_attributes_to_gu

## linux x86_64 (azure)

- [pystats raw](bm-20240501-azure-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9-pystats.json)
- [pystats table](bm-20240501-azure-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9-pystats.md)

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/faster-cpython/benchmarking/actions/runs/8910285083)
- cpu model: Intel(R) Xeon(R) W-2255 CPU @ 3.70GHz
- platform: Linux-5.4.0-164-generic-x86_64-with-glibc2.31
- [raw results](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9.json)

### vs. 3.10.4

- Geometric mean: 1.34x faster (HPT: reliability of 100.00%, 1.26x faster at 99th %ile)
- Memory usage: 1.10x
- missing benchmarks: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9-vs-3.10.4.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9-vs-3.10.4.svg)

### vs. 3.12.0

- Geometric mean: 1.03x faster (HPT: reliability of 99.86%, 1.00x faster at 99th %ile)
- Memory usage: 0.96x
- missing benchmarks: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
- new benchmarks: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9-vs-3.12.0.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9-vs-3.12.0.svg)

### vs. 3.13.0b2

- Geometric mean: 1.01x faster (HPT: reliability of 98.75%, 1.00x faster at 99th %ile)
- Memory usage: 0.98x
- missing benchmarks: bpe_tokeniser, flaskblogging
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9-vs-3.13.0b2.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9-vs-3.13.0b2.svg)

### vs. base

- Geometric mean: 1.00x slower (HPT: reliability of 99.43%, 1.00x slower at 99th %ile)
- Memory usage: 1.00x
- [🧠memory plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9-vs-base-mem.svg)
- [📄table](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9-vs-base.md)
- [📈time plot](bm-20240501-linux-x86_64-faster%252dcpython-use_attributes_to_gu-3.13.0a6%2B-5032ad9-vs-base.svg)

