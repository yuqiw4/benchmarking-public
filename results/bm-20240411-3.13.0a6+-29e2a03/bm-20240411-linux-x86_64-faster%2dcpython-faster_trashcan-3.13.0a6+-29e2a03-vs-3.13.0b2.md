# Results vs. 3.13.0b2

- fork: faster-cpython
- ref: faster_trashcan
- machine: linux-x86_64
- commit hash: 29e2a03
- commit date: 2024-04-11
- overall geometric mean: 1.01x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 268 ms: 1.02x faster                                                        |
| chameleon      | 7.22 ms                                                    | 6.80 ms: 1.06x faster                                                       |
| docutils       | 2.83 sec                                                   | 2.81 sec: 1.00x faster                                                      |
| html5lib       | 67.2 ms                                                    | 68.1 ms: 1.01x slower                                                       |
| tornado_http   | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                                       |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 354 ms: 1.07x faster                                                        |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                        |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                |

Benchmark hidden because not significant (6): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 78.0 ms: 1.01x faster                                                       |
| pidigits       | 191 ms                                                     | 203 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 135 ms: 1.02x faster                                                        |
| regex_dna      | 221 ms                                                     | 223 ms: 1.01x slower                                                        |
| regex_v8       | 25.1 ms                                                    | 25.9 ms: 1.03x slower                                                       |
| regex_effbot   | 3.67 ms                                                    | 3.81 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_list          | 5.11 us                                                    | 4.94 us: 1.03x faster                                                       |
| pickle_pure_python   | 305 us                                                     | 298 us: 1.02x faster                                                        |
| xml_etree_parse      | 162 ms                                                     | 159 ms: 1.02x faster                                                        |
| pickle_dict          | 34.8 us                                                    | 34.2 us: 1.02x faster                                                       |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                       |
| xml_etree_process    | 61.2 ms                                                    | 60.5 ms: 1.01x faster                                                       |
| xml_etree_generate   | 87.4 ms                                                    | 87.2 ms: 1.00x faster                                                       |
| pickle               | 11.5 us                                                    | 11.6 us: 1.01x slower                                                       |
| tomli_loads          | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                                      |
| unpickle_pure_python | 218 us                                                     | 224 us: 1.03x slower                                                        |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                                |

Benchmark hidden because not significant (4): xml_etree_iterparse, json_loads, unpickle_list, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|------------------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                       |
| python_startup_no_site | 7.11 ms                                                    | 7.06 ms: 1.01x faster                                                       |
| Geometric mean         | (ref)                                                      | 1.02x faster                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                       |
| genshi_text    | 23.7 ms                                                    | 23.4 ms: 1.01x faster                                                       |
| genshi_xml     | 51.6 ms                                                    | 51.3 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                      | 1.02x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240411-linux-x86_64-faster%2dcpython-faster_trashcan-3.13.0a6+-29e2a03 |
|----------------------------|:----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 113 us: 1.45x faster                                                        |
| pylint                     | 317 ms                                                     | 277 ms: 1.14x faster                                                        |
| richards                   | 50.9 ms                                                    | 46.5 ms: 1.09x faster                                                       |
| logging_silent             | 105 ns                                                     | 96.0 ns: 1.09x faster                                                       |
| richards_super             | 57.4 ms                                                    | 52.9 ms: 1.09x faster                                                       |
| mdp                        | 2.79 sec                                                   | 2.58 sec: 1.08x faster                                                      |
| async_tree_none            | 378 ms                                                     | 354 ms: 1.07x faster                                                        |
| chameleon                  | 7.22 ms                                                    | 6.80 ms: 1.06x faster                                                       |
| deepcopy_memo              | 39.7 us                                                    | 37.6 us: 1.06x faster                                                       |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                       |
| scimark_lu                 | 122 ms                                                     | 116 ms: 1.05x faster                                                        |
| scimark_sor                | 127 ms                                                     | 122 ms: 1.04x faster                                                        |
| scimark_fft                | 392 ms                                                     | 378 ms: 1.04x faster                                                        |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                       |
| pickle_list                | 5.11 us                                                    | 4.94 us: 1.03x faster                                                       |
| fannkuch                   | 402 ms                                                     | 390 ms: 1.03x faster                                                        |
| spectral_norm              | 116 ms                                                     | 113 ms: 1.03x faster                                                        |
| deepcopy_reduce            | 3.35 us                                                    | 3.26 us: 1.03x faster                                                       |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.03x faster                                                       |
| sqlglot_transpile          | 1.63 ms                                                    | 1.59 ms: 1.02x faster                                                       |
| pickle_pure_python         | 305 us                                                     | 298 us: 1.02x faster                                                        |
| deltablue                  | 3.25 ms                                                    | 3.17 ms: 1.02x faster                                                       |
| chaos                      | 61.3 ms                                                    | 60.0 ms: 1.02x faster                                                       |
| go                         | 145 ms                                                     | 142 ms: 1.02x faster                                                        |
| 2to3                       | 274 ms                                                     | 268 ms: 1.02x faster                                                        |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                                       |
| raytrace                   | 267 ms                                                     | 261 ms: 1.02x faster                                                        |
| crypto_pyaes               | 77.5 ms                                                    | 75.9 ms: 1.02x faster                                                       |
| deepcopy                   | 367 us                                                     | 360 us: 1.02x faster                                                        |
| pprint_pformat             | 1.56 sec                                                   | 1.53 sec: 1.02x faster                                                      |
| xml_etree_parse            | 162 ms                                                     | 159 ms: 1.02x faster                                                        |
| pprint_safe_repr           | 758 ms                                                     | 746 ms: 1.02x faster                                                        |
| pickle_dict                | 34.8 us                                                    | 34.2 us: 1.02x faster                                                       |
| logging_format             | 6.47 us                                                    | 6.37 us: 1.02x faster                                                       |
| regex_compile              | 137 ms                                                     | 135 ms: 1.02x faster                                                        |
| thrift                     | 823 us                                                     | 811 us: 1.02x faster                                                        |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                                       |
| genshi_text                | 23.7 ms                                                    | 23.4 ms: 1.01x faster                                                       |
| float                      | 78.9 ms                                                    | 78.0 ms: 1.01x faster                                                       |
| sympy_str                  | 282 ms                                                     | 279 ms: 1.01x faster                                                        |
| xml_etree_process          | 61.2 ms                                                    | 60.5 ms: 1.01x faster                                                       |
| gunicorn                   | 1.28 ms                                                    | 1.26 ms: 1.01x faster                                                       |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.5 ms: 1.01x faster                                                       |
| pyflate                    | 484 ms                                                     | 479 ms: 1.01x faster                                                        |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                       |
| sympy_expand               | 473 ms                                                     | 469 ms: 1.01x faster                                                        |
| gc_traversal               | 3.98 ms                                                    | 3.95 ms: 1.01x faster                                                       |
| sympy_integrate            | 20.5 ms                                                    | 20.4 ms: 1.01x faster                                                       |
| python_startup_no_site     | 7.11 ms                                                    | 7.06 ms: 1.01x faster                                                       |
| genshi_xml                 | 51.6 ms                                                    | 51.3 ms: 1.01x faster                                                       |
| sqlglot_optimize           | 55.5 ms                                                    | 55.2 ms: 1.01x faster                                                       |
| dulwich_log                | 67.2 ms                                                    | 66.8 ms: 1.01x faster                                                       |
| async_generators           | 442 ms                                                     | 439 ms: 1.01x faster                                                        |
| hexiom                     | 6.30 ms                                                    | 6.26 ms: 1.01x faster                                                       |
| asyncio_tcp                | 508 ms                                                     | 505 ms: 1.01x faster                                                        |
| docutils                   | 2.83 sec                                                   | 2.81 sec: 1.00x faster                                                      |
| tornado_http               | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                                       |
| sqlglot_normalize          | 110 ms                                                     | 110 ms: 1.00x faster                                                        |
| xml_etree_generate         | 87.4 ms                                                    | 87.2 ms: 1.00x faster                                                       |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x slower                                                      |
| comprehensions             | 16.6 us                                                    | 16.7 us: 1.00x slower                                                       |
| meteor_contest             | 110 ms                                                     | 110 ms: 1.01x slower                                                        |
| regex_dna                  | 221 ms                                                     | 223 ms: 1.01x slower                                                        |
| json                       | 5.31 ms                                                    | 5.35 ms: 1.01x slower                                                       |
| nqueens                    | 81.4 ms                                                    | 82.2 ms: 1.01x slower                                                       |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.33 ms: 1.01x slower                                                       |
| pickle                     | 11.5 us                                                    | 11.6 us: 1.01x slower                                                       |
| html5lib                   | 67.2 ms                                                    | 68.1 ms: 1.01x slower                                                       |
| tomli_loads                | 2.12 sec                                                   | 2.16 sec: 1.02x slower                                                      |
| generators                 | 29.6 ms                                                    | 30.3 ms: 1.02x slower                                                       |
| unpickle_pure_python       | 218 us                                                     | 224 us: 1.03x slower                                                        |
| regex_v8                   | 25.1 ms                                                    | 25.9 ms: 1.03x slower                                                       |
| regex_effbot               | 3.67 ms                                                    | 3.81 ms: 1.04x slower                                                       |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 610 ms: 1.04x slower                                                        |
| telco                      | 8.41 ms                                                    | 8.74 ms: 1.04x slower                                                       |
| coverage                   | 93.1 ms                                                    | 97.6 ms: 1.05x slower                                                       |
| pidigits                   | 191 ms                                                     | 203 ms: 1.06x slower                                                        |
| pathlib                    | 17.3 ms                                                    | 18.7 ms: 1.08x slower                                                       |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                                |

Benchmark hidden because not significant (21): async_tree_io, pycparser, mypy2, xml_etree_iterparse, sympy_sum, dask, async_tree_memoization_tg, nbody, json_loads, bench_mp_pool, async_tree_none_tg, unpickle_list, async_tree_memoization, logging_simple, asyncio_websockets, sqlite_synth, coroutines, bench_thread_pool, unpickle, async_tree_cpu_io_mixed, async_tree_io_tg
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x