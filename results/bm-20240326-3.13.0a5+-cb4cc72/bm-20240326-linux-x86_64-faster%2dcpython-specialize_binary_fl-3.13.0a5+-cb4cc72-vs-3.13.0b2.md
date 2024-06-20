# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: specialize_binary_fl
- machine: linux-x86_64
- commit hash: cb4cc72
- commit date: 2024-03-26
- overall geometric mean: 1.01x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-specialize_binary_fl-3.13.0a5+-cb4cc72 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 269 ms: 1.02x faster                                                             |
| chameleon      | 7.22 ms                                                    | 6.94 ms: 1.04x faster                                                            |
| docutils       | 2.83 sec                                                   | 2.77 sec: 1.02x faster                                                           |
| html5lib       | 67.2 ms                                                    | 66.0 ms: 1.02x faster                                                            |
| tornado_http   | 94.6 ms                                                    | 95.3 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-specialize_binary_fl-3.13.0a5+-cb4cc72 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 613 ms: 1.04x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 352 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                      | 1.00x slower                                                                     |

Benchmark hidden because not significant (6): async_tree_io, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_none, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-specialize_binary_fl-3.13.0a5+-cb4cc72 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.2 ms: 1.02x faster                                                            |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                             |
| nbody          | 88.3 ms                                                    | 91.2 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-specialize_binary_fl-3.13.0a5+-cb4cc72 |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| regex_effbot   | 3.67 ms                                                    | 3.69 ms: 1.01x slower                                                            |
| regex_v8       | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                            |
| regex_dna      | 221 ms                                                     | 226 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-specialize_binary_fl-3.13.0a5+-cb4cc72 |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_process    | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                            |
| xml_etree_generate   | 87.4 ms                                                    | 85.7 ms: 1.02x faster                                                            |
| json_loads           | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| pickle_pure_python   | 305 us                                                     | 302 us: 1.01x faster                                                             |
| pickle_list          | 5.11 us                                                    | 5.16 us: 1.01x slower                                                            |
| pickle_dict          | 34.8 us                                                    | 35.2 us: 1.01x slower                                                            |
| unpickle_pure_python | 218 us                                                     | 221 us: 1.01x slower                                                             |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                            |
| unpickle_list        | 5.34 us                                                    | 5.50 us: 1.03x slower                                                            |
| tomli_loads          | 2.12 sec                                                   | 2.21 sec: 1.04x slower                                                           |
| unpickle             | 15.1 us                                                    | 16.0 us: 1.06x slower                                                            |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                                     |

Benchmark hidden because not significant (3): xml_etree_parse, json_dumps, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-specialize_binary_fl-3.13.0a5+-cb4cc72 |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| python_startup_no_site | 7.11 ms                                                    | 8.95 ms: 1.26x slower                                                            |
| Geometric mean         | (ref)                                                      | 1.11x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-specialize_binary_fl-3.13.0a5+-cb4cc72 |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 51.6 ms                                                    | 50.8 ms: 1.02x faster                                                            |
| django_template | 34.8 ms                                                    | 34.6 ms: 1.01x faster                                                            |
| mako            | 11.2 ms                                                    | 11.3 ms: 1.00x slower                                                            |
| genshi_text     | 23.7 ms                                                    | 24.2 ms: 1.02x slower                                                            |
| Geometric mean  | (ref)                                                      | 1.00x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-faster%2dcpython-specialize_binary_fl-3.13.0a5+-cb4cc72 |
|----------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 109 us: 1.52x faster                                                             |
| create_gc_cycles           | 1.82 ms                                                    | 1.46 ms: 1.24x faster                                                            |
| gc_traversal               | 3.98 ms                                                    | 3.58 ms: 1.11x faster                                                            |
| richards_super             | 57.4 ms                                                    | 51.8 ms: 1.11x faster                                                            |
| richards                   | 50.9 ms                                                    | 46.0 ms: 1.11x faster                                                            |
| scimark_lu                 | 122 ms                                                     | 113 ms: 1.08x faster                                                             |
| scimark_fft                | 392 ms                                                     | 367 ms: 1.07x faster                                                             |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.93 ms: 1.07x faster                                                            |
| crypto_pyaes               | 77.5 ms                                                    | 72.8 ms: 1.06x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                    | 3.19 us: 1.05x faster                                                            |
| chameleon                  | 7.22 ms                                                    | 6.94 ms: 1.04x faster                                                            |
| logging_silent             | 105 ns                                                     | 101 ns: 1.04x faster                                                             |
| scimark_sor                | 127 ms                                                     | 123 ms: 1.04x faster                                                             |
| pprint_safe_repr           | 758 ms                                                     | 731 ms: 1.04x faster                                                             |
| sqlglot_parse              | 1.32 ms                                                    | 1.27 ms: 1.04x faster                                                            |
| sqlglot_transpile          | 1.63 ms                                                    | 1.58 ms: 1.03x faster                                                            |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                           |
| go                         | 145 ms                                                     | 140 ms: 1.03x faster                                                             |
| deepcopy                   | 367 us                                                     | 356 us: 1.03x faster                                                             |
| spectral_norm              | 116 ms                                                     | 113 ms: 1.03x faster                                                             |
| scimark_monte_carlo        | 69.2 ms                                                    | 67.4 ms: 1.03x faster                                                            |
| sqlite_synth               | 2.99 us                                                    | 2.92 us: 1.02x faster                                                            |
| sympy_str                  | 282 ms                                                     | 276 ms: 1.02x faster                                                             |
| float                      | 78.9 ms                                                    | 77.2 ms: 1.02x faster                                                            |
| docutils                   | 2.83 sec                                                   | 2.77 sec: 1.02x faster                                                           |
| xml_etree_process          | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                            |
| sympy_expand               | 473 ms                                                     | 463 ms: 1.02x faster                                                             |
| sympy_integrate            | 20.5 ms                                                    | 20.1 ms: 1.02x faster                                                            |
| xml_etree_generate         | 87.4 ms                                                    | 85.7 ms: 1.02x faster                                                            |
| 2to3                       | 274 ms                                                     | 269 ms: 1.02x faster                                                             |
| html5lib                   | 67.2 ms                                                    | 66.0 ms: 1.02x faster                                                            |
| thrift                     | 823 us                                                     | 808 us: 1.02x faster                                                             |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                             |
| sympy_sum                  | 156 ms                                                     | 153 ms: 1.02x faster                                                             |
| chaos                      | 61.3 ms                                                    | 60.4 ms: 1.02x faster                                                            |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                                            |
| genshi_xml                 | 51.6 ms                                                    | 50.8 ms: 1.02x faster                                                            |
| deepcopy_memo              | 39.7 us                                                    | 39.2 us: 1.01x faster                                                            |
| sqlglot_normalize          | 110 ms                                                     | 109 ms: 1.01x faster                                                             |
| pyflate                    | 484 ms                                                     | 478 ms: 1.01x faster                                                             |
| json_loads                 | 28.9 us                                                    | 28.5 us: 1.01x faster                                                            |
| pickle_pure_python         | 305 us                                                     | 302 us: 1.01x faster                                                             |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                             |
| coroutines                 | 23.2 ms                                                    | 23.0 ms: 1.01x faster                                                            |
| sqlglot_optimize           | 55.5 ms                                                    | 55.0 ms: 1.01x faster                                                            |
| comprehensions             | 16.6 us                                                    | 16.5 us: 1.01x faster                                                            |
| nqueens                    | 81.4 ms                                                    | 80.7 ms: 1.01x faster                                                            |
| django_template            | 34.8 ms                                                    | 34.6 ms: 1.01x faster                                                            |
| asyncio_tcp                | 508 ms                                                     | 505 ms: 1.01x faster                                                             |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.83 sec: 1.00x faster                                                           |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.00x faster                                                             |
| mdp                        | 2.79 sec                                                   | 2.78 sec: 1.00x faster                                                           |
| mako                       | 11.2 ms                                                    | 11.3 ms: 1.00x slower                                                            |
| regex_effbot               | 3.67 ms                                                    | 3.69 ms: 1.01x slower                                                            |
| tornado_http               | 94.6 ms                                                    | 95.3 ms: 1.01x slower                                                            |
| generators                 | 29.6 ms                                                    | 29.9 ms: 1.01x slower                                                            |
| pickle_list                | 5.11 us                                                    | 5.16 us: 1.01x slower                                                            |
| pickle_dict                | 34.8 us                                                    | 35.2 us: 1.01x slower                                                            |
| dulwich_log                | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                                            |
| logging_format             | 6.47 us                                                    | 6.56 us: 1.01x slower                                                            |
| unpickle_pure_python       | 218 us                                                     | 221 us: 1.01x slower                                                             |
| telco                      | 8.41 ms                                                    | 8.55 ms: 1.02x slower                                                            |
| regex_v8                   | 25.1 ms                                                    | 25.6 ms: 1.02x slower                                                            |
| regex_dna                  | 221 ms                                                     | 226 ms: 1.02x slower                                                             |
| genshi_text                | 23.7 ms                                                    | 24.2 ms: 1.02x slower                                                            |
| pycparser                  | 1.16 sec                                                   | 1.18 sec: 1.02x slower                                                           |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                            |
| logging_simple             | 5.74 us                                                    | 5.91 us: 1.03x slower                                                            |
| unpickle_list              | 5.34 us                                                    | 5.50 us: 1.03x slower                                                            |
| nbody                      | 88.3 ms                                                    | 91.2 ms: 1.03x slower                                                            |
| coverage                   | 93.1 ms                                                    | 96.4 ms: 1.04x slower                                                            |
| tomli_loads                | 2.12 sec                                                   | 2.21 sec: 1.04x slower                                                           |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 613 ms: 1.04x slower                                                             |
| async_tree_none_tg         | 336 ms                                                     | 352 ms: 1.05x slower                                                             |
| unpickle                   | 15.1 us                                                    | 16.0 us: 1.06x slower                                                            |
| pathlib                    | 17.3 ms                                                    | 18.7 ms: 1.08x slower                                                            |
| python_startup_no_site     | 7.11 ms                                                    | 8.95 ms: 1.26x slower                                                            |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                     |

Benchmark hidden because not significant (24): async_tree_io, async_tree_cpu_io_mixed, async_tree_io_tg, xml_etree_parse, djangocms, async_tree_none, dask, json_dumps, asyncio_websockets, bench_thread_pool, deltablue, mypy2, raytrace, xml_etree_iterparse, fannkuch, gunicorn, async_tree_memoization, bench_mp_pool, async_generators, json, async_tree_memoization_tg, aiohttp, hexiom, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240326-3.13.0a5+-cb4cc72/bm-20240326-linux-x86_64-faster%2dcpython-specialize_binary_fl-3.13.0a5+-cb4cc72.json: unpack_sequence

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.97x