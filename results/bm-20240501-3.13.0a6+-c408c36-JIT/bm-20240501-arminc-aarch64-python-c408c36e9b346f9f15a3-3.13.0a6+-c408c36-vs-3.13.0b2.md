# Results vs. 3.13.0b2

- fork: python
- ref: c408c36e9b346f9f15a3
- machine: linux-aarch64
- commit hash: c408c36
- commit date: 2024-05-01
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 305 ms                                                       | 348 ms: 1.14x slower                                                     |
| chameleon      | 8.95 ms                                                      | 9.37 ms: 1.05x slower                                                    |
| docutils       | 3.10 sec                                                     | 3.40 sec: 1.10x slower                                                   |
| html5lib       | 66.1 ms                                                      | 70.4 ms: 1.07x slower                                                    |
| tornado_http   | 128 ms                                                       | 140 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                        | 1.09x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg | 1.27 sec                                                     | 1.20 sec: 1.06x faster                                                   |
| async_tree_none  | 492 ms                                                       | 508 ms: 1.03x slower                                                     |
| Geometric mean   | (ref)                                                        | 1.01x slower                                                             |

Benchmark hidden because not significant (6): async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 114 ms                                                       | 107 ms: 1.06x faster                                                     |
| float          | 91.4 ms                                                      | 89.2 ms: 1.03x faster                                                    |
| pidigits       | 234 ms                                                       | 233 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                        | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 259 ms                                                       | 247 ms: 1.05x faster                                                     |
| regex_v8       | 31.1 ms                                                      | 30.2 ms: 1.03x faster                                                    |
| regex_effbot   | 4.98 ms                                                      | 4.85 ms: 1.03x faster                                                    |
| regex_compile  | 128 ms                                                       | 160 ms: 1.25x slower                                                     |
| Geometric mean | (ref)                                                        | 1.03x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_list        | 6.52 us                                                      | 6.31 us: 1.03x faster                                                    |
| json_dumps           | 13.1 ms                                                      | 12.8 ms: 1.02x faster                                                    |
| pickle_pure_python   | 359 us                                                       | 354 us: 1.01x faster                                                     |
| json_loads           | 32.1 us                                                      | 31.9 us: 1.01x faster                                                    |
| pickle_list          | 5.27 us                                                      | 5.23 us: 1.01x faster                                                    |
| unpickle             | 19.8 us                                                      | 19.7 us: 1.00x faster                                                    |
| unpickle_pure_python | 251 us                                                       | 276 us: 1.10x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                             |

Benchmark hidden because not significant (7): xml_etree_parse, xml_etree_process, xml_etree_generate, tomli_loads, xml_etree_iterparse, pickle_dict, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 13.0 ms                                                      | 14.7 ms: 1.13x slower                                                    |
| python_startup_no_site | 8.60 ms                                                      | 10.7 ms: 1.24x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 13.2 ms                                                      | 12.8 ms: 1.03x faster                                                    |
| django_template | 42.3 ms                                                      | 48.3 ms: 1.14x slower                                                    |
| genshi_text     | 27.4 ms                                                      | 33.8 ms: 1.23x slower                                                    |
| genshi_xml      | 60.4 ms                                                      | 79.5 ms: 1.32x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|--------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| richards                 | 55.9 ms                                                      | 52.5 ms: 1.06x faster                                                    |
| nbody                    | 114 ms                                                       | 107 ms: 1.06x faster                                                     |
| async_tree_io_tg         | 1.27 sec                                                     | 1.20 sec: 1.06x faster                                                   |
| richards_super           | 62.3 ms                                                      | 59.3 ms: 1.05x faster                                                    |
| regex_dna                | 259 ms                                                       | 247 ms: 1.05x faster                                                     |
| unpickle_list            | 6.52 us                                                      | 6.31 us: 1.03x faster                                                    |
| mako                     | 13.2 ms                                                      | 12.8 ms: 1.03x faster                                                    |
| regex_v8                 | 31.1 ms                                                      | 30.2 ms: 1.03x faster                                                    |
| regex_effbot             | 4.98 ms                                                      | 4.85 ms: 1.03x faster                                                    |
| float                    | 91.4 ms                                                      | 89.2 ms: 1.03x faster                                                    |
| gc_traversal             | 5.17 ms                                                      | 5.05 ms: 1.02x faster                                                    |
| sqlite_synth             | 3.90 us                                                      | 3.81 us: 1.02x faster                                                    |
| json_dumps               | 13.1 ms                                                      | 12.8 ms: 1.02x faster                                                    |
| pickle_pure_python       | 359 us                                                       | 354 us: 1.01x faster                                                     |
| json_loads               | 32.1 us                                                      | 31.9 us: 1.01x faster                                                    |
| pickle_list              | 5.27 us                                                      | 5.23 us: 1.01x faster                                                    |
| pidigits                 | 234 ms                                                       | 233 ms: 1.01x faster                                                     |
| unpickle                 | 19.8 us                                                      | 19.7 us: 1.00x faster                                                    |
| coverage                 | 98.4 ms                                                      | 99.2 ms: 1.01x slower                                                    |
| spectral_norm            | 141 ms                                                       | 143 ms: 1.01x slower                                                     |
| scimark_fft              | 445 ms                                                       | 453 ms: 1.02x slower                                                     |
| fannkuch                 | 451 ms                                                       | 461 ms: 1.02x slower                                                     |
| pathlib                  | 22.8 ms                                                      | 23.3 ms: 1.02x slower                                                    |
| thrift                   | 962 us                                                       | 985 us: 1.02x slower                                                     |
| scimark_monte_carlo      | 82.3 ms                                                      | 84.4 ms: 1.03x slower                                                    |
| generators               | 37.1 ms                                                      | 38.1 ms: 1.03x slower                                                    |
| asyncio_tcp_ssl          | 2.21 sec                                                     | 2.27 sec: 1.03x slower                                                   |
| deepcopy                 | 448 us                                                       | 461 us: 1.03x slower                                                     |
| telco                    | 10.0 ms                                                      | 10.3 ms: 1.03x slower                                                    |
| mdp                      | 3.33 sec                                                     | 3.43 sec: 1.03x slower                                                   |
| coroutines               | 29.0 ms                                                      | 29.9 ms: 1.03x slower                                                    |
| async_tree_none          | 492 ms                                                       | 508 ms: 1.03x slower                                                     |
| async_generators         | 488 ms                                                       | 510 ms: 1.04x slower                                                     |
| deepcopy_reduce          | 4.04 us                                                      | 4.22 us: 1.04x slower                                                    |
| meteor_contest           | 113 ms                                                       | 119 ms: 1.05x slower                                                     |
| chameleon                | 8.95 ms                                                      | 9.37 ms: 1.05x slower                                                    |
| pycparser                | 1.22 sec                                                     | 1.28 sec: 1.05x slower                                                   |
| bench_thread_pool        | 1.26 ms                                                      | 1.33 ms: 1.06x slower                                                    |
| logging_simple           | 7.21 us                                                      | 7.61 us: 1.06x slower                                                    |
| sqlglot_normalize        | 129 ms                                                       | 137 ms: 1.06x slower                                                     |
| sqlglot_parse            | 1.42 ms                                                      | 1.51 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult  | 6.55 ms                                                      | 6.96 ms: 1.06x slower                                                    |
| dask                     | 370 ms                                                       | 394 ms: 1.06x slower                                                     |
| pyflate                  | 557 ms                                                       | 592 ms: 1.06x slower                                                     |
| logging_format           | 7.82 us                                                      | 8.34 us: 1.07x slower                                                    |
| html5lib                 | 66.1 ms                                                      | 70.4 ms: 1.07x slower                                                    |
| asyncio_tcp              | 584 ms                                                       | 622 ms: 1.07x slower                                                     |
| crypto_pyaes             | 82.0 ms                                                      | 87.5 ms: 1.07x slower                                                    |
| raytrace                 | 297 ms                                                       | 317 ms: 1.07x slower                                                     |
| sqlglot_optimize         | 62.6 ms                                                      | 68.0 ms: 1.09x slower                                                    |
| tornado_http             | 128 ms                                                       | 140 ms: 1.09x slower                                                     |
| docutils                 | 3.10 sec                                                     | 3.40 sec: 1.10x slower                                                   |
| unpickle_pure_python     | 251 us                                                       | 276 us: 1.10x slower                                                     |
| typing_runtime_protocols | 193 us                                                       | 213 us: 1.10x slower                                                     |
| sqlglot_transpile        | 1.71 ms                                                      | 1.88 ms: 1.10x slower                                                    |
| python_startup           | 13.0 ms                                                      | 14.7 ms: 1.13x slower                                                    |
| sympy_expand             | 457 ms                                                       | 520 ms: 1.14x slower                                                     |
| django_template          | 42.3 ms                                                      | 48.3 ms: 1.14x slower                                                    |
| 2to3                     | 305 ms                                                       | 348 ms: 1.14x slower                                                     |
| comprehensions           | 20.5 us                                                      | 23.5 us: 1.14x slower                                                    |
| scimark_sor              | 159 ms                                                       | 183 ms: 1.15x slower                                                     |
| sympy_str                | 265 ms                                                       | 307 ms: 1.16x slower                                                     |
| go                       | 161 ms                                                       | 187 ms: 1.16x slower                                                     |
| deltablue                | 3.88 ms                                                      | 4.59 ms: 1.18x slower                                                    |
| chaos                    | 68.3 ms                                                      | 82.1 ms: 1.20x slower                                                    |
| dulwich_log              | 58.5 ms                                                      | 70.5 ms: 1.20x slower                                                    |
| pylint                   | 337 ms                                                       | 408 ms: 1.21x slower                                                     |
| sympy_sum                | 144 ms                                                       | 174 ms: 1.21x slower                                                     |
| nqueens                  | 98.9 ms                                                      | 120 ms: 1.22x slower                                                     |
| sympy_integrate          | 20.9 ms                                                      | 25.5 ms: 1.22x slower                                                    |
| genshi_text              | 27.4 ms                                                      | 33.8 ms: 1.23x slower                                                    |
| bench_mp_pool            | 7.03 ms                                                      | 8.69 ms: 1.24x slower                                                    |
| python_startup_no_site   | 8.60 ms                                                      | 10.7 ms: 1.24x slower                                                    |
| regex_compile            | 128 ms                                                       | 160 ms: 1.25x slower                                                     |
| pprint_pformat           | 1.93 sec                                                     | 2.43 sec: 1.26x slower                                                   |
| pprint_safe_repr         | 933 ms                                                       | 1.18 sec: 1.26x slower                                                   |
| hexiom                   | 7.08 ms                                                      | 8.94 ms: 1.26x slower                                                    |
| scimark_lu               | 141 ms                                                       | 181 ms: 1.28x slower                                                     |
| genshi_xml               | 60.4 ms                                                      | 79.5 ms: 1.32x slower                                                    |
| Geometric mean           | (ref)                                                        | 1.06x slower                                                             |

Benchmark hidden because not significant (18): xml_etree_parse, create_gc_cycles, async_tree_none_tg, xml_etree_process, xml_etree_generate, logging_silent, tomli_loads, deepcopy_memo, xml_etree_iterparse, asyncio_websockets, pickle_dict, json, pickle, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization
Ignored benchmarks (5) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17.json: aiohttp, bpe_tokeniser, flaskblogging, gunicorn, mypy2

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.07x