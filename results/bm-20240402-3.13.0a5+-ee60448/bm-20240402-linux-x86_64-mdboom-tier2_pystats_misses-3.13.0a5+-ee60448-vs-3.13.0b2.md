# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_pystats_misses
- machine: linux-x86_64
- commit hash: ee60448
- commit date: 2024-04-02
- overall geometric mean: 1.02x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 267 ms: 1.02x faster                                                   |
| chameleon      | 7.22 ms                                                    | 6.90 ms: 1.05x faster                                                  |
| docutils       | 2.83 sec                                                   | 2.79 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                      | 1.02x faster                                                           |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 348 ms: 1.09x faster                                                   |
| async_tree_none_tg         | 336 ms                                                     | 331 ms: 1.02x faster                                                   |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 604 ms: 1.03x slower                                                   |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                           |

Benchmark hidden because not significant (5): async_tree_io, async_tree_memoization, async_tree_memoization_tg, async_tree_io_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.3 ms: 1.02x faster                                                  |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 132 ms: 1.03x faster                                                   |
| regex_dna      | 221 ms                                                     | 224 ms: 1.01x slower                                                   |
| regex_effbot   | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                                  |
| regex_v8       | 25.1 ms                                                    | 25.5 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.07 us: 1.05x faster                                                  |
| xml_etree_process    | 61.2 ms                                                    | 59.4 ms: 1.03x faster                                                  |
| json_dumps           | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| pickle_pure_python   | 305 us                                                     | 299 us: 1.02x faster                                                   |
| xml_etree_iterparse  | 107 ms                                                     | 106 ms: 1.01x faster                                                   |
| xml_etree_generate   | 87.4 ms                                                    | 86.3 ms: 1.01x faster                                                  |
| unpickle_pure_python | 218 us                                                     | 216 us: 1.01x faster                                                   |
| pickle_dict          | 34.8 us                                                    | 35.2 us: 1.01x slower                                                  |
| tomli_loads          | 2.12 sec                                                   | 2.15 sec: 1.01x slower                                                 |
| pickle_list          | 5.11 us                                                    | 5.26 us: 1.03x slower                                                  |
| unpickle             | 15.1 us                                                    | 15.7 us: 1.04x slower                                                  |
| pickle               | 11.5 us                                                    | 12.0 us: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                      | 1.00x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                  |
| python_startup_no_site | 7.11 ms                                                    | 9.00 ms: 1.27x slower                                                  |
| Geometric mean         | (ref)                                                      | 1.12x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                  |
| genshi_xml     | 51.6 ms                                                    | 52.0 ms: 1.01x slower                                                  |
| genshi_text    | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                      | 1.00x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240402-linux-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 114 us: 1.45x faster                                                   |
| pylint                     | 317 ms                                                     | 278 ms: 1.14x faster                                                   |
| richards                   | 50.9 ms                                                    | 45.7 ms: 1.11x faster                                                  |
| richards_super             | 57.4 ms                                                    | 51.8 ms: 1.11x faster                                                  |
| scimark_lu                 | 122 ms                                                     | 112 ms: 1.09x faster                                                   |
| async_tree_none            | 378 ms                                                     | 348 ms: 1.09x faster                                                   |
| scimark_fft                | 392 ms                                                     | 361 ms: 1.09x faster                                                   |
| crypto_pyaes               | 77.5 ms                                                    | 72.3 ms: 1.07x faster                                                  |
| deepcopy_memo              | 39.7 us                                                    | 37.2 us: 1.07x faster                                                  |
| mdp                        | 2.79 sec                                                   | 2.62 sec: 1.06x faster                                                 |
| spectral_norm              | 116 ms                                                     | 109 ms: 1.06x faster                                                   |
| logging_silent             | 105 ns                                                     | 98.6 ns: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 4.98 ms: 1.06x faster                                                  |
| unpickle_list              | 5.34 us                                                    | 5.07 us: 1.05x faster                                                  |
| sqlglot_parse              | 1.32 ms                                                    | 1.25 ms: 1.05x faster                                                  |
| deepcopy                   | 367 us                                                     | 349 us: 1.05x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                    | 3.19 us: 1.05x faster                                                  |
| raytrace                   | 267 ms                                                     | 254 ms: 1.05x faster                                                   |
| chameleon                  | 7.22 ms                                                    | 6.90 ms: 1.05x faster                                                  |
| sqlglot_transpile          | 1.63 ms                                                    | 1.57 ms: 1.04x faster                                                  |
| pyflate                    | 484 ms                                                     | 465 ms: 1.04x faster                                                   |
| fannkuch                   | 402 ms                                                     | 386 ms: 1.04x faster                                                   |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                                  |
| deltablue                  | 3.25 ms                                                    | 3.13 ms: 1.04x faster                                                  |
| scimark_monte_carlo        | 69.2 ms                                                    | 66.7 ms: 1.04x faster                                                  |
| regex_compile              | 137 ms                                                     | 132 ms: 1.03x faster                                                   |
| chaos                      | 61.3 ms                                                    | 59.4 ms: 1.03x faster                                                  |
| pprint_pformat             | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                                 |
| pprint_safe_repr           | 758 ms                                                     | 737 ms: 1.03x faster                                                   |
| xml_etree_process          | 61.2 ms                                                    | 59.4 ms: 1.03x faster                                                  |
| hexiom                     | 6.30 ms                                                    | 6.12 ms: 1.03x faster                                                  |
| sympy_str                  | 282 ms                                                     | 275 ms: 1.03x faster                                                   |
| sympy_expand               | 473 ms                                                     | 461 ms: 1.03x faster                                                   |
| sqlglot_optimize           | 55.5 ms                                                    | 54.1 ms: 1.03x faster                                                  |
| sqlglot_normalize          | 110 ms                                                     | 107 ms: 1.03x faster                                                   |
| go                         | 145 ms                                                     | 141 ms: 1.03x faster                                                   |
| 2to3                       | 274 ms                                                     | 267 ms: 1.02x faster                                                   |
| json_dumps                 | 10.7 ms                                                    | 10.5 ms: 1.02x faster                                                  |
| mako                       | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                                  |
| sympy_integrate            | 20.5 ms                                                    | 20.0 ms: 1.02x faster                                                  |
| sqlite_synth               | 2.99 us                                                    | 2.92 us: 1.02x faster                                                  |
| nqueens                    | 81.4 ms                                                    | 79.7 ms: 1.02x faster                                                  |
| pickle_pure_python         | 305 us                                                     | 299 us: 1.02x faster                                                   |
| float                      | 78.9 ms                                                    | 77.3 ms: 1.02x faster                                                  |
| coroutines                 | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                  |
| sympy_sum                  | 156 ms                                                     | 153 ms: 1.02x faster                                                   |
| async_tree_none_tg         | 336 ms                                                     | 331 ms: 1.02x faster                                                   |
| thrift                     | 823 us                                                     | 810 us: 1.02x faster                                                   |
| docutils                   | 2.83 sec                                                   | 2.79 sec: 1.01x faster                                                 |
| xml_etree_iterparse        | 107 ms                                                     | 106 ms: 1.01x faster                                                   |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.01x faster                                                  |
| xml_etree_generate         | 87.4 ms                                                    | 86.3 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 218 us                                                     | 216 us: 1.01x faster                                                   |
| pidigits                   | 191 ms                                                     | 189 ms: 1.01x faster                                                   |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                                  |
| meteor_contest             | 110 ms                                                     | 109 ms: 1.01x faster                                                   |
| gunicorn                   | 1.28 ms                                                    | 1.27 ms: 1.01x faster                                                  |
| bench_thread_pool          | 834 us                                                     | 826 us: 1.01x faster                                                   |
| async_generators           | 442 ms                                                     | 438 ms: 1.01x faster                                                   |
| logging_format             | 6.47 us                                                    | 6.42 us: 1.01x faster                                                  |
| asyncio_websockets         | 567 ms                                                     | 563 ms: 1.01x faster                                                   |
| scimark_sor                | 127 ms                                                     | 127 ms: 1.00x faster                                                   |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.85 sec: 1.00x slower                                                 |
| generators                 | 29.6 ms                                                    | 29.8 ms: 1.01x slower                                                  |
| logging_simple             | 5.74 us                                                    | 5.79 us: 1.01x slower                                                  |
| genshi_xml                 | 51.6 ms                                                    | 52.0 ms: 1.01x slower                                                  |
| gc_traversal               | 3.98 ms                                                    | 4.01 ms: 1.01x slower                                                  |
| genshi_text                | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                                  |
| pickle_dict                | 34.8 us                                                    | 35.2 us: 1.01x slower                                                  |
| regex_dna                  | 221 ms                                                     | 224 ms: 1.01x slower                                                   |
| tomli_loads                | 2.12 sec                                                   | 2.15 sec: 1.01x slower                                                 |
| regex_effbot               | 3.67 ms                                                    | 3.73 ms: 1.02x slower                                                  |
| dulwich_log                | 67.2 ms                                                    | 68.3 ms: 1.02x slower                                                  |
| regex_v8                   | 25.1 ms                                                    | 25.5 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 604 ms: 1.03x slower                                                   |
| pickle_list                | 5.11 us                                                    | 5.26 us: 1.03x slower                                                  |
| coverage                   | 93.1 ms                                                    | 96.4 ms: 1.04x slower                                                  |
| unpickle                   | 15.1 us                                                    | 15.7 us: 1.04x slower                                                  |
| json                       | 5.31 ms                                                    | 5.53 ms: 1.04x slower                                                  |
| pycparser                  | 1.16 sec                                                   | 1.21 sec: 1.04x slower                                                 |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.05x slower                                                  |
| pathlib                    | 17.3 ms                                                    | 18.5 ms: 1.07x slower                                                  |
| python_startup_no_site     | 7.11 ms                                                    | 9.00 ms: 1.27x slower                                                  |
| Geometric mean             | (ref)                                                      | 1.02x faster                                                           |

Benchmark hidden because not significant (16): async_tree_io, async_tree_memoization, mypy2, async_tree_memoization_tg, async_tree_io_tg, dask, xml_etree_parse, async_tree_cpu_io_mixed, json_loads, tornado_http, telco, asyncio_tcp, html5lib, nbody, bench_mp_pool, comprehensions
Ignored benchmarks (4) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, djangocms, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x