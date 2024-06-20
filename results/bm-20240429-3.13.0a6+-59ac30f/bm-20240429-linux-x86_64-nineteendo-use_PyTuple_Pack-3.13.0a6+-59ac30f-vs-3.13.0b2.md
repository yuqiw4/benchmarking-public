# Results vs. 3.13.0b2

- fork: nineteendo
- ref: use_PyTuple_Pack
- machine: linux-x86_64
- commit hash: 59ac30f
- commit date: 2024-04-29
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 267 ms: 1.02x faster                                                   |
| chameleon      | 7.22 ms                                                    | 6.98 ms: 1.03x faster                                                  |
| docutils       | 2.83 sec                                                   | 2.79 sec: 1.01x faster                                                 |
| tornado_http   | 94.6 ms                                                    | 93.9 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 349 ms: 1.08x faster                                                   |
| async_tree_io              | 939 ms                                                     | 898 ms: 1.05x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                           |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.7 ms: 1.01x faster                                                  |
| pidigits       | 191 ms                                                     | 212 ms: 1.11x slower                                                   |
| Geometric mean | (ref)                                                      | 1.03x slower                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.4 ms: 1.03x faster                                                  |
| regex_compile  | 137 ms                                                     | 134 ms: 1.02x faster                                                   |
| regex_dna      | 221 ms                                                     | 218 ms: 1.02x faster                                                   |
| regex_effbot   | 3.67 ms                                                    | 3.65 ms: 1.01x faster                                                  |
| Geometric mean | (ref)                                                      | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                    | 27.4 us: 1.05x faster                                                  |
| xml_etree_process    | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                  |
| pickle_pure_python   | 305 us                                                     | 300 us: 1.02x faster                                                   |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| pickle_list          | 5.11 us                                                    | 5.02 us: 1.02x faster                                                  |
| xml_etree_parse      | 162 ms                                                     | 159 ms: 1.02x faster                                                   |
| unpickle_pure_python | 218 us                                                     | 215 us: 1.02x faster                                                   |
| pickle_dict          | 34.8 us                                                    | 34.6 us: 1.01x faster                                                  |
| unpickle_list        | 5.34 us                                                    | 5.38 us: 1.01x slower                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.15 sec: 1.02x slower                                                 |
| pickle               | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_generate, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| python_startup_no_site | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                  |
| genshi_xml      | 51.6 ms                                                    | 51.1 ms: 1.01x faster                                                  |
| django_template | 34.8 ms                                                    | 34.5 ms: 1.01x faster                                                  |
| genshi_text     | 23.7 ms                                                    | 23.5 ms: 1.01x faster                                                  |
| Geometric mean  | (ref)                                                      | 1.02x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240429-linux-x86_64-nineteendo-use_PyTuple_Pack-3.13.0a6+-59ac30f |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| richards                   | 50.9 ms                                                    | 46.6 ms: 1.09x faster                                                  |
| async_tree_none            | 378 ms                                                     | 349 ms: 1.08x faster                                                   |
| mdp                        | 2.79 sec                                                   | 2.57 sec: 1.08x faster                                                 |
| richards_super             | 57.4 ms                                                    | 53.1 ms: 1.08x faster                                                  |
| logging_silent             | 105 ns                                                     | 97.2 ns: 1.08x faster                                                  |
| scimark_fft                | 392 ms                                                     | 365 ms: 1.07x faster                                                   |
| spectral_norm              | 116 ms                                                     | 108 ms: 1.07x faster                                                   |
| deepcopy_memo              | 39.7 us                                                    | 37.2 us: 1.07x faster                                                  |
| deepcopy_reduce            | 3.35 us                                                    | 3.17 us: 1.06x faster                                                  |
| json_loads                 | 28.9 us                                                    | 27.4 us: 1.05x faster                                                  |
| scimark_lu                 | 122 ms                                                     | 116 ms: 1.05x faster                                                   |
| mako                       | 11.2 ms                                                    | 10.7 ms: 1.05x faster                                                  |
| async_tree_io              | 939 ms                                                     | 898 ms: 1.05x faster                                                   |
| deepcopy                   | 367 us                                                     | 353 us: 1.04x faster                                                   |
| sqlglot_parse              | 1.32 ms                                                    | 1.27 ms: 1.04x faster                                                  |
| pprint_pformat             | 1.56 sec                                                   | 1.50 sec: 1.04x faster                                                 |
| sqlglot_transpile          | 1.63 ms                                                    | 1.57 ms: 1.04x faster                                                  |
| pyflate                    | 484 ms                                                     | 466 ms: 1.04x faster                                                   |
| coroutines                 | 23.2 ms                                                    | 22.4 ms: 1.04x faster                                                  |
| chameleon                  | 7.22 ms                                                    | 6.98 ms: 1.03x faster                                                  |
| create_gc_cycles           | 1.82 ms                                                    | 1.76 ms: 1.03x faster                                                  |
| pprint_safe_repr           | 758 ms                                                     | 735 ms: 1.03x faster                                                   |
| raytrace                   | 267 ms                                                     | 259 ms: 1.03x faster                                                   |
| fannkuch                   | 402 ms                                                     | 390 ms: 1.03x faster                                                   |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.12 ms: 1.03x faster                                                  |
| go                         | 145 ms                                                     | 141 ms: 1.03x faster                                                   |
| scimark_sor                | 127 ms                                                     | 124 ms: 1.03x faster                                                   |
| regex_v8                   | 25.1 ms                                                    | 24.4 ms: 1.03x faster                                                  |
| crypto_pyaes               | 77.5 ms                                                    | 75.4 ms: 1.03x faster                                                  |
| 2to3                       | 274 ms                                                     | 267 ms: 1.02x faster                                                   |
| json                       | 5.31 ms                                                    | 5.18 ms: 1.02x faster                                                  |
| xml_etree_process          | 61.2 ms                                                    | 59.8 ms: 1.02x faster                                                  |
| python_startup             | 10.8 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| hexiom                     | 6.30 ms                                                    | 6.15 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.99 us                                                    | 2.93 us: 1.02x faster                                                  |
| deltablue                  | 3.25 ms                                                    | 3.19 ms: 1.02x faster                                                  |
| chaos                      | 61.3 ms                                                    | 60.1 ms: 1.02x faster                                                  |
| sqlglot_optimize           | 55.5 ms                                                    | 54.4 ms: 1.02x faster                                                  |
| pycparser                  | 1.16 sec                                                   | 1.14 sec: 1.02x faster                                                 |
| sympy_str                  | 282 ms                                                     | 277 ms: 1.02x faster                                                   |
| pickle_pure_python         | 305 us                                                     | 300 us: 1.02x faster                                                   |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| regex_compile              | 137 ms                                                     | 134 ms: 1.02x faster                                                   |
| pickle_list                | 5.11 us                                                    | 5.02 us: 1.02x faster                                                  |
| coverage                   | 93.1 ms                                                    | 91.6 ms: 1.02x faster                                                  |
| regex_dna                  | 221 ms                                                     | 218 ms: 1.02x faster                                                   |
| xml_etree_parse            | 162 ms                                                     | 159 ms: 1.02x faster                                                   |
| unpickle_pure_python       | 218 us                                                     | 215 us: 1.02x faster                                                   |
| float                      | 78.9 ms                                                    | 77.7 ms: 1.01x faster                                                  |
| sympy_integrate            | 20.5 ms                                                    | 20.2 ms: 1.01x faster                                                  |
| sqlglot_normalize          | 110 ms                                                     | 109 ms: 1.01x faster                                                   |
| dulwich_log                | 67.2 ms                                                    | 66.3 ms: 1.01x faster                                                  |
| sympy_expand               | 473 ms                                                     | 467 ms: 1.01x faster                                                   |
| docutils                   | 2.83 sec                                                   | 2.79 sec: 1.01x faster                                                 |
| sympy_sum                  | 156 ms                                                     | 154 ms: 1.01x faster                                                   |
| genshi_xml                 | 51.6 ms                                                    | 51.1 ms: 1.01x faster                                                  |
| nqueens                    | 81.4 ms                                                    | 80.7 ms: 1.01x faster                                                  |
| django_template            | 34.8 ms                                                    | 34.5 ms: 1.01x faster                                                  |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                  |
| genshi_text                | 23.7 ms                                                    | 23.5 ms: 1.01x faster                                                  |
| tornado_http               | 94.6 ms                                                    | 93.9 ms: 1.01x faster                                                  |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                   |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                  |
| regex_effbot               | 3.67 ms                                                    | 3.65 ms: 1.01x faster                                                  |
| pickle_dict                | 34.8 us                                                    | 34.6 us: 1.01x faster                                                  |
| asyncio_tcp                | 508 ms                                                     | 506 ms: 1.00x faster                                                   |
| bench_thread_pool          | 834 us                                                     | 831 us: 1.00x faster                                                   |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x faster                                                 |
| meteor_contest             | 110 ms                                                     | 110 ms: 1.00x faster                                                   |
| python_startup_no_site     | 7.11 ms                                                    | 7.09 ms: 1.00x faster                                                  |
| async_generators           | 442 ms                                                     | 444 ms: 1.00x slower                                                   |
| comprehensions             | 16.6 us                                                    | 16.7 us: 1.01x slower                                                  |
| unpickle_list              | 5.34 us                                                    | 5.38 us: 1.01x slower                                                  |
| pathlib                    | 17.3 ms                                                    | 17.5 ms: 1.01x slower                                                  |
| gc_traversal               | 3.98 ms                                                    | 4.02 ms: 1.01x slower                                                  |
| tomli_loads                | 2.12 sec                                                   | 2.15 sec: 1.02x slower                                                 |
| logging_simple             | 5.74 us                                                    | 5.84 us: 1.02x slower                                                  |
| pickle                     | 11.5 us                                                    | 11.7 us: 1.02x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 603 ms: 1.03x slower                                                   |
| pidigits                   | 191 ms                                                     | 212 ms: 1.11x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                           |

Benchmark hidden because not significant (21): async_tree_memoization_tg, async_tree_none_tg, mypy2, xml_etree_iterparse, dask, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_io_tg, xml_etree_generate, logging_format, nbody, thrift, bench_mp_pool, typing_runtime_protocols, djangocms, pylint, generators, html5lib, scimark_monte_carlo, telco, unpickle
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x