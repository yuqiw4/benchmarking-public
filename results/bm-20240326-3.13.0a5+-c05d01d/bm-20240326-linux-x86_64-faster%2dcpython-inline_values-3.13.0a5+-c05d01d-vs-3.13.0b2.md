# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: inline_values
- machine: linux-x86_64
- commit hash: c05d01d
- commit date: 2024-03-26
- overall geometric mean: 1.02x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-inline_values-3.13.0a5+-c05d01d |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 268 ms: 1.02x faster                                                      |
| chameleon      | 7.22 ms                                                    | 6.88 ms: 1.05x faster                                                     |
| docutils       | 2.83 sec                                                   | 2.78 sec: 1.02x faster                                                    |
| html5lib       | 67.2 ms                                                    | 66.1 ms: 1.02x faster                                                     |
| tornado_http   | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                      | 1.02x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-inline_values-3.13.0a5+-c05d01d |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 336 ms                                                     | 347 ms: 1.03x slower                                                      |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 611 ms: 1.04x slower                                                      |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                              |

Benchmark hidden because not significant (6): async_tree_io_tg, async_tree_memoization_tg, async_tree_none, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-inline_values-3.13.0a5+-c05d01d |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 78.1 ms: 1.01x faster                                                     |
| nbody          | 88.3 ms                                                    | 89.3 ms: 1.01x slower                                                     |
| pidigits       | 191 ms                                                     | 194 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                      | 1.00x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-inline_values-3.13.0a5+-c05d01d |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 133 ms: 1.03x faster                                                      |
| regex_dna      | 221 ms                                                     | 221 ms: 1.00x faster                                                      |
| regex_effbot   | 3.67 ms                                                    | 3.72 ms: 1.01x slower                                                     |
| regex_v8       | 25.1 ms                                                    | 25.5 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                      | 1.00x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-inline_values-3.13.0a5+-c05d01d |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle_pure_python   | 305 us                                                     | 298 us: 1.02x faster                                                      |
| xml_etree_process    | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                     |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                     |
| unpickle_list        | 5.34 us                                                    | 5.25 us: 1.02x faster                                                     |
| json_loads           | 28.9 us                                                    | 28.6 us: 1.01x faster                                                     |
| xml_etree_generate   | 87.4 ms                                                    | 86.6 ms: 1.01x faster                                                     |
| unpickle_pure_python | 218 us                                                     | 216 us: 1.01x faster                                                      |
| pickle_dict          | 34.8 us                                                    | 34.6 us: 1.00x faster                                                     |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                                     |
| pickle_list          | 5.11 us                                                    | 5.25 us: 1.03x slower                                                     |
| tomli_loads          | 2.12 sec                                                   | 2.18 sec: 1.03x slower                                                    |
| unpickle             | 15.1 us                                                    | 16.2 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                              |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-inline_values-3.13.0a5+-c05d01d |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                     |
| python_startup_no_site | 7.11 ms                                                    | 8.87 ms: 1.25x slower                                                     |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-inline_values-3.13.0a5+-c05d01d |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                     |
| genshi_text    | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                     |
| genshi_xml     | 51.6 ms                                                    | 53.2 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                      | 1.01x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-inline_values-3.13.0a5+-c05d01d |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 111 us: 1.49x faster                                                      |
| create_gc_cycles           | 1.82 ms                                                    | 1.53 ms: 1.19x faster                                                     |
| richards                   | 50.9 ms                                                    | 45.7 ms: 1.11x faster                                                     |
| scimark_lu                 | 122 ms                                                     | 110 ms: 1.11x faster                                                      |
| richards_super             | 57.4 ms                                                    | 51.7 ms: 1.11x faster                                                     |
| scimark_fft                | 392 ms                                                     | 354 ms: 1.11x faster                                                      |
| crypto_pyaes               | 77.5 ms                                                    | 71.0 ms: 1.09x faster                                                     |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.84 ms: 1.09x faster                                                     |
| gc_traversal               | 3.98 ms                                                    | 3.67 ms: 1.08x faster                                                     |
| pyflate                    | 484 ms                                                     | 451 ms: 1.07x faster                                                      |
| scimark_sor                | 127 ms                                                     | 119 ms: 1.07x faster                                                      |
| deepcopy_memo              | 39.7 us                                                    | 37.2 us: 1.07x faster                                                     |
| logging_silent             | 105 ns                                                     | 98.5 ns: 1.06x faster                                                     |
| mdp                        | 2.79 sec                                                   | 2.63 sec: 1.06x faster                                                    |
| scimark_monte_carlo        | 69.2 ms                                                    | 65.5 ms: 1.06x faster                                                     |
| deepcopy_reduce            | 3.35 us                                                    | 3.17 us: 1.06x faster                                                     |
| deepcopy                   | 367 us                                                     | 349 us: 1.05x faster                                                      |
| spectral_norm              | 116 ms                                                     | 111 ms: 1.05x faster                                                      |
| chameleon                  | 7.22 ms                                                    | 6.88 ms: 1.05x faster                                                     |
| sqlglot_parse              | 1.32 ms                                                    | 1.26 ms: 1.05x faster                                                     |
| sqlglot_transpile          | 1.63 ms                                                    | 1.57 ms: 1.04x faster                                                     |
| go                         | 145 ms                                                     | 139 ms: 1.04x faster                                                      |
| deltablue                  | 3.25 ms                                                    | 3.12 ms: 1.04x faster                                                     |
| mako                       | 11.2 ms                                                    | 10.8 ms: 1.04x faster                                                     |
| coroutines                 | 23.2 ms                                                    | 22.3 ms: 1.04x faster                                                     |
| raytrace                   | 267 ms                                                     | 257 ms: 1.04x faster                                                      |
| chaos                      | 61.3 ms                                                    | 59.3 ms: 1.04x faster                                                     |
| fannkuch                   | 402 ms                                                     | 389 ms: 1.03x faster                                                      |
| hexiom                     | 6.30 ms                                                    | 6.10 ms: 1.03x faster                                                     |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                    |
| pycparser                  | 1.16 sec                                                   | 1.13 sec: 1.03x faster                                                    |
| pprint_safe_repr           | 758 ms                                                     | 739 ms: 1.03x faster                                                      |
| regex_compile              | 137 ms                                                     | 133 ms: 1.03x faster                                                      |
| sqlite_synth               | 2.99 us                                                    | 2.92 us: 1.02x faster                                                     |
| pickle_pure_python         | 305 us                                                     | 298 us: 1.02x faster                                                      |
| xml_etree_process          | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                     |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                     |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                     |
| sympy_integrate            | 20.5 ms                                                    | 20.1 ms: 1.02x faster                                                     |
| sympy_str                  | 282 ms                                                     | 277 ms: 1.02x faster                                                      |
| 2to3                       | 274 ms                                                     | 268 ms: 1.02x faster                                                      |
| meteor_contest             | 110 ms                                                     | 108 ms: 1.02x faster                                                      |
| sympy_expand               | 473 ms                                                     | 463 ms: 1.02x faster                                                      |
| thrift                     | 823 us                                                     | 808 us: 1.02x faster                                                      |
| unpickle_list              | 5.34 us                                                    | 5.25 us: 1.02x faster                                                     |
| docutils                   | 2.83 sec                                                   | 2.78 sec: 1.02x faster                                                    |
| html5lib                   | 67.2 ms                                                    | 66.1 ms: 1.02x faster                                                     |
| sympy_sum                  | 156 ms                                                     | 154 ms: 1.01x faster                                                      |
| comprehensions             | 16.6 us                                                    | 16.4 us: 1.01x faster                                                     |
| sqlglot_optimize           | 55.5 ms                                                    | 54.8 ms: 1.01x faster                                                     |
| float                      | 78.9 ms                                                    | 78.1 ms: 1.01x faster                                                     |
| json_loads                 | 28.9 us                                                    | 28.6 us: 1.01x faster                                                     |
| xml_etree_generate         | 87.4 ms                                                    | 86.6 ms: 1.01x faster                                                     |
| unpickle_pure_python       | 218 us                                                     | 216 us: 1.01x faster                                                      |
| bench_thread_pool          | 834 us                                                     | 826 us: 1.01x faster                                                      |
| sqlglot_normalize          | 110 ms                                                     | 109 ms: 1.01x faster                                                      |
| tornado_http               | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                                     |
| pickle_dict                | 34.8 us                                                    | 34.6 us: 1.00x faster                                                     |
| regex_dna                  | 221 ms                                                     | 221 ms: 1.00x faster                                                      |
| asyncio_websockets         | 567 ms                                                     | 569 ms: 1.00x slower                                                      |
| dulwich_log                | 67.2 ms                                                    | 67.7 ms: 1.01x slower                                                     |
| async_generators           | 442 ms                                                     | 446 ms: 1.01x slower                                                      |
| asyncio_tcp                | 508 ms                                                     | 513 ms: 1.01x slower                                                      |
| telco                      | 8.41 ms                                                    | 8.50 ms: 1.01x slower                                                     |
| nbody                      | 88.3 ms                                                    | 89.3 ms: 1.01x slower                                                     |
| pidigits                   | 191 ms                                                     | 194 ms: 1.01x slower                                                      |
| regex_effbot               | 3.67 ms                                                    | 3.72 ms: 1.01x slower                                                     |
| regex_v8                   | 25.1 ms                                                    | 25.5 ms: 1.01x slower                                                     |
| logging_simple             | 5.74 us                                                    | 5.87 us: 1.02x slower                                                     |
| genshi_text                | 23.7 ms                                                    | 24.3 ms: 1.03x slower                                                     |
| pickle                     | 11.5 us                                                    | 11.8 us: 1.03x slower                                                     |
| pickle_list                | 5.11 us                                                    | 5.25 us: 1.03x slower                                                     |
| tomli_loads                | 2.12 sec                                                   | 2.18 sec: 1.03x slower                                                    |
| genshi_xml                 | 51.6 ms                                                    | 53.2 ms: 1.03x slower                                                     |
| json                       | 5.31 ms                                                    | 5.47 ms: 1.03x slower                                                     |
| async_tree_none_tg         | 336 ms                                                     | 347 ms: 1.03x slower                                                      |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 611 ms: 1.04x slower                                                      |
| coverage                   | 93.1 ms                                                    | 98.3 ms: 1.06x slower                                                     |
| unpickle                   | 15.1 us                                                    | 16.2 us: 1.07x slower                                                     |
| pathlib                    | 17.3 ms                                                    | 18.6 ms: 1.08x slower                                                     |
| python_startup_no_site     | 7.11 ms                                                    | 8.87 ms: 1.25x slower                                                     |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                              |

Benchmark hidden because not significant (18): async_tree_io_tg, async_tree_memoization_tg, mypy2, async_tree_none, aiohttp, async_tree_io, async_tree_cpu_io_mixed, bench_mp_pool, gunicorn, dask, async_tree_memoization, asyncio_tcp_ssl, generators, logging_format, xml_etree_iterparse, nqueens, xml_etree_parse, pylint
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging
Ignored benchmarks (1) of results/bm-20240326-3.13.0a5+-c05d01d/bm-20240326-linux-x86_64-faster%2dcpython-inline_values-3.13.0a5+-c05d01d.json: unpack_sequence

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.97x