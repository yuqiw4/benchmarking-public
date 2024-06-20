# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: call_stat_inc
- machine: linux-x86_64
- commit hash: 34584c3
- commit date: 2024-04-16
- overall geometric mean: 1.01x faster
- HPT reliability: 96.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 271 ms: 1.01x faster                                                |
| chameleon      | 7.22 ms                                                    | 6.96 ms: 1.04x faster                                               |
| tornado_http   | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                               |
| Geometric mean | (ref)                                                      | 1.01x faster                                                        |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 378 ms                                                     | 357 ms: 1.06x faster                                                |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.02x slower                                                |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                        |

Benchmark hidden because not significant (6): async_tree_io_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 191 ms                                                     | 193 ms: 1.01x slower                                                |
| nbody          | 88.3 ms                                                    | 91.1 ms: 1.03x slower                                               |
| Geometric mean | (ref)                                                      | 1.01x slower                                                        |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_v8       | 25.1 ms                                                    | 24.9 ms: 1.01x faster                                               |
| regex_compile  | 137 ms                                                     | 136 ms: 1.01x faster                                                |
| regex_dna      | 221 ms                                                     | 222 ms: 1.00x slower                                                |
| regex_effbot   | 3.67 ms                                                    | 3.71 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                      | 1.00x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.03 us: 1.06x faster                                               |
| json_loads           | 28.9 us                                                    | 27.8 us: 1.04x faster                                               |
| pickle_pure_python   | 305 us                                                     | 302 us: 1.01x faster                                                |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                               |
| xml_etree_process    | 61.2 ms                                                    | 60.8 ms: 1.01x faster                                               |
| unpickle_pure_python | 218 us                                                     | 220 us: 1.01x slower                                                |
| xml_etree_iterparse  | 107 ms                                                     | 108 ms: 1.01x slower                                                |
| xml_etree_generate   | 87.4 ms                                                    | 88.7 ms: 1.01x slower                                               |
| pickle_dict          | 34.8 us                                                    | 35.4 us: 1.02x slower                                               |
| tomli_loads          | 2.12 sec                                                   | 2.21 sec: 1.04x slower                                              |
| pickle               | 11.5 us                                                    | 12.0 us: 1.05x slower                                               |
| pickle_list          | 5.11 us                                                    | 5.40 us: 1.06x slower                                               |
| unpickle             | 15.1 us                                                    | 17.0 us: 1.13x slower                                               |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                        |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                               |
| python_startup_no_site | 7.11 ms                                                    | 7.13 ms: 1.00x slower                                               |
| Geometric mean         | (ref)                                                      | 1.01x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|-----------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                               |
| django_template | 34.8 ms                                                    | 35.1 ms: 1.01x slower                                               |
| genshi_text     | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                               |
| genshi_xml      | 51.6 ms                                                    | 52.9 ms: 1.02x slower                                               |
| Geometric mean  | (ref)                                                      | 1.01x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240416-linux-x86_64-gvanrossum-call_stat_inc-3.13.0a6+-34584c3 |
|----------------------------|:----------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 165 us                                                     | 116 us: 1.42x faster                                                |
| mdp                        | 2.79 sec                                                   | 2.59 sec: 1.07x faster                                              |
| unpickle_list              | 5.34 us                                                    | 5.03 us: 1.06x faster                                               |
| scimark_fft                | 392 ms                                                     | 370 ms: 1.06x faster                                                |
| async_tree_none            | 378 ms                                                     | 357 ms: 1.06x faster                                                |
| scimark_lu                 | 122 ms                                                     | 115 ms: 1.06x faster                                                |
| richards_super             | 57.4 ms                                                    | 54.4 ms: 1.06x faster                                               |
| deepcopy_reduce            | 3.35 us                                                    | 3.18 us: 1.05x faster                                               |
| richards                   | 50.9 ms                                                    | 48.4 ms: 1.05x faster                                               |
| scimark_sor                | 127 ms                                                     | 122 ms: 1.04x faster                                                |
| json_loads                 | 28.9 us                                                    | 27.8 us: 1.04x faster                                               |
| deepcopy                   | 367 us                                                     | 354 us: 1.04x faster                                                |
| fannkuch                   | 402 ms                                                     | 387 ms: 1.04x faster                                                |
| pyflate                    | 484 ms                                                     | 467 ms: 1.04x faster                                                |
| deepcopy_memo              | 39.7 us                                                    | 38.3 us: 1.04x faster                                               |
| chameleon                  | 7.22 ms                                                    | 6.96 ms: 1.04x faster                                               |
| crypto_pyaes               | 77.5 ms                                                    | 74.7 ms: 1.04x faster                                               |
| create_gc_cycles           | 1.82 ms                                                    | 1.75 ms: 1.04x faster                                               |
| logging_silent             | 105 ns                                                     | 102 ns: 1.03x faster                                                |
| spectral_norm              | 116 ms                                                     | 113 ms: 1.03x faster                                                |
| sqlglot_transpile          | 1.63 ms                                                    | 1.60 ms: 1.02x faster                                               |
| sqlglot_parse              | 1.32 ms                                                    | 1.29 ms: 1.02x faster                                               |
| mako                       | 11.2 ms                                                    | 11.0 ms: 1.02x faster                                               |
| scimark_sparse_mat_mult    | 5.27 ms                                                    | 5.17 ms: 1.02x faster                                               |
| python_startup             | 10.8 ms                                                    | 10.6 ms: 1.02x faster                                               |
| chaos                      | 61.3 ms                                                    | 60.2 ms: 1.02x faster                                               |
| sqlite_synth               | 2.99 us                                                    | 2.94 us: 1.02x faster                                               |
| raytrace                   | 267 ms                                                     | 263 ms: 1.01x faster                                                |
| pickle_pure_python         | 305 us                                                     | 302 us: 1.01x faster                                                |
| json                       | 5.31 ms                                                    | 5.25 ms: 1.01x faster                                               |
| 2to3                       | 274 ms                                                     | 271 ms: 1.01x faster                                                |
| scimark_monte_carlo        | 69.2 ms                                                    | 68.5 ms: 1.01x faster                                               |
| coroutines                 | 23.2 ms                                                    | 23.0 ms: 1.01x faster                                               |
| json_dumps                 | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                               |
| logging_format             | 6.47 us                                                    | 6.42 us: 1.01x faster                                               |
| regex_v8                   | 25.1 ms                                                    | 24.9 ms: 1.01x faster                                               |
| go                         | 145 ms                                                     | 143 ms: 1.01x faster                                                |
| dulwich_log                | 67.2 ms                                                    | 66.7 ms: 1.01x faster                                               |
| aiohttp                    | 1.18 ms                                                    | 1.17 ms: 1.01x faster                                               |
| regex_compile              | 137 ms                                                     | 136 ms: 1.01x faster                                                |
| xml_etree_process          | 61.2 ms                                                    | 60.8 ms: 1.01x faster                                               |
| asyncio_websockets         | 567 ms                                                     | 564 ms: 1.01x faster                                                |
| pprint_safe_repr           | 758 ms                                                     | 754 ms: 1.01x faster                                                |
| tornado_http               | 94.6 ms                                                    | 94.2 ms: 1.00x faster                                               |
| gc_traversal               | 3.98 ms                                                    | 3.96 ms: 1.00x faster                                               |
| asyncio_tcp_ssl            | 1.84 sec                                                   | 1.84 sec: 1.00x faster                                              |
| python_startup_no_site     | 7.11 ms                                                    | 7.13 ms: 1.00x slower                                               |
| regex_dna                  | 221 ms                                                     | 222 ms: 1.00x slower                                                |
| bench_thread_pool          | 834 us                                                     | 838 us: 1.00x slower                                                |
| logging_simple             | 5.74 us                                                    | 5.78 us: 1.01x slower                                               |
| sympy_sum                  | 156 ms                                                     | 157 ms: 1.01x slower                                                |
| unpickle_pure_python       | 218 us                                                     | 220 us: 1.01x slower                                                |
| pidigits                   | 191 ms                                                     | 193 ms: 1.01x slower                                                |
| django_template            | 34.8 ms                                                    | 35.1 ms: 1.01x slower                                               |
| xml_etree_iterparse        | 107 ms                                                     | 108 ms: 1.01x slower                                                |
| regex_effbot               | 3.67 ms                                                    | 3.71 ms: 1.01x slower                                               |
| sqlglot_normalize          | 110 ms                                                     | 111 ms: 1.01x slower                                                |
| genshi_text                | 23.7 ms                                                    | 23.9 ms: 1.01x slower                                               |
| hexiom                     | 6.30 ms                                                    | 6.37 ms: 1.01x slower                                               |
| pathlib                    | 17.3 ms                                                    | 17.5 ms: 1.01x slower                                               |
| deltablue                  | 3.25 ms                                                    | 3.29 ms: 1.01x slower                                               |
| xml_etree_generate         | 87.4 ms                                                    | 88.7 ms: 1.01x slower                                               |
| meteor_contest             | 110 ms                                                     | 111 ms: 1.01x slower                                                |
| pickle_dict                | 34.8 us                                                    | 35.4 us: 1.02x slower                                               |
| genshi_xml                 | 51.6 ms                                                    | 52.9 ms: 1.02x slower                                               |
| async_tree_cpu_io_mixed_tg | 587 ms                                                     | 602 ms: 1.02x slower                                                |
| telco                      | 8.41 ms                                                    | 8.65 ms: 1.03x slower                                               |
| comprehensions             | 16.6 us                                                    | 17.1 us: 1.03x slower                                               |
| nbody                      | 88.3 ms                                                    | 91.1 ms: 1.03x slower                                               |
| coverage                   | 93.1 ms                                                    | 96.8 ms: 1.04x slower                                               |
| tomli_loads                | 2.12 sec                                                   | 2.21 sec: 1.04x slower                                              |
| pickle                     | 11.5 us                                                    | 12.0 us: 1.05x slower                                               |
| pickle_list                | 5.11 us                                                    | 5.40 us: 1.06x slower                                               |
| unpickle                   | 15.1 us                                                    | 17.0 us: 1.13x slower                                               |
| Geometric mean             | (ref)                                                      | 1.01x faster                                                        |

Benchmark hidden because not significant (27): async_tree_io_tg, async_tree_io, dask, async_tree_cpu_io_mixed, gunicorn, async_tree_memoization, pprint_pformat, asyncio_tcp, sympy_integrate, sympy_str, bench_mp_pool, async_tree_memoization_tg, mypy2, async_tree_none_tg, thrift, sympy_expand, html5lib, float, docutils, async_generators, nqueens, generators, sqlglot_optimize, pycparser, xml_etree_parse, pylint, djangocms
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 96.82% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.98x