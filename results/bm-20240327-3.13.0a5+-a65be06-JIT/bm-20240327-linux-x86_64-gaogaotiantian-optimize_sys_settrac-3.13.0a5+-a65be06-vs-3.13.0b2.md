# Results vs. 3.13.0b2

- fork: gaogaotiantian
- ref: optimize_sys_settrac
- machine: linux-x86_64
- commit hash: a65be06
- commit date: 2024-03-27
- overall geometric mean: 1.01x slower
- HPT reliability: 99.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 280 ms: 1.02x slower                                                           |
| chameleon      | 7.22 ms                                                    | 7.00 ms: 1.03x faster                                                          |
| docutils       | 2.83 sec                                                   | 2.89 sec: 1.02x slower                                                         |
| html5lib       | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                                          |
| tornado_http   | 94.6 ms                                                    | 96.9 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                      | 1.01x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|--------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none    | 378 ms                                                     | 357 ms: 1.06x faster                                                           |
| async_tree_io_tg   | 936 ms                                                     | 900 ms: 1.04x faster                                                           |
| async_tree_none_tg | 336 ms                                                     | 347 ms: 1.03x slower                                                           |
| Geometric mean     | (ref)                                                      | 1.01x faster                                                                   |

Benchmark hidden because not significant (5): async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 76.4 ms: 1.03x faster                                                          |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                           |
| nbody          | 88.3 ms                                                    | 92.5 ms: 1.05x slower                                                          |
| Geometric mean | (ref)                                                      | 1.00x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.62 ms: 1.01x faster                                                          |
| regex_dna      | 221 ms                                                     | 219 ms: 1.01x faster                                                           |
| regex_v8       | 25.1 ms                                                    | 25.5 ms: 1.02x slower                                                          |
| regex_compile  | 137 ms                                                     | 147 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                      | 1.02x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_list        | 5.34 us                                                    | 5.21 us: 1.03x faster                                                          |
| tomli_loads          | 2.12 sec                                                   | 2.09 sec: 1.01x faster                                                         |
| pickle_list          | 5.11 us                                                    | 5.04 us: 1.01x faster                                                          |
| xml_etree_process    | 61.2 ms                                                    | 60.8 ms: 1.01x faster                                                          |
| xml_etree_generate   | 87.4 ms                                                    | 88.8 ms: 1.02x slower                                                          |
| pickle_pure_python   | 305 us                                                     | 311 us: 1.02x slower                                                           |
| unpickle             | 15.1 us                                                    | 15.5 us: 1.03x slower                                                          |
| pickle_dict          | 34.8 us                                                    | 36.0 us: 1.03x slower                                                          |
| pickle               | 11.5 us                                                    | 11.9 us: 1.04x slower                                                          |
| unpickle_pure_python | 218 us                                                     | 245 us: 1.12x slower                                                           |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                                   |

Benchmark hidden because not significant (4): json_dumps, xml_etree_iterparse, xml_etree_parse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.1 ms: 1.04x slower                                                          |
| python_startup_no_site | 7.11 ms                                                    | 9.56 ms: 1.35x slower                                                          |
| Geometric mean         | (ref)                                                      | 1.18x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|-----------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                          |
| django_template | 34.8 ms                                                    | 36.0 ms: 1.04x slower                                                          |
| genshi_text     | 23.7 ms                                                    | 25.0 ms: 1.06x slower                                                          |
| genshi_xml      | 51.6 ms                                                    | 55.8 ms: 1.08x slower                                                          |
| Geometric mean  | (ref)                                                      | 1.03x slower                                                                   |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|--------------------------|:----------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 111 us: 1.49x faster                                                           |
| scimark_fft              | 392 ms                                                     | 343 ms: 1.14x faster                                                           |
| richards                 | 50.9 ms                                                    | 47.2 ms: 1.08x faster                                                          |
| richards_super           | 57.4 ms                                                    | 53.2 ms: 1.08x faster                                                          |
| create_gc_cycles         | 1.82 ms                                                    | 1.70 ms: 1.07x faster                                                          |
| async_tree_none          | 378 ms                                                     | 357 ms: 1.06x faster                                                           |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 5.01 ms: 1.05x faster                                                          |
| mdp                      | 2.79 sec                                                   | 2.66 sec: 1.05x faster                                                         |
| deepcopy_reduce          | 3.35 us                                                    | 3.21 us: 1.04x faster                                                          |
| async_tree_io_tg         | 936 ms                                                     | 900 ms: 1.04x faster                                                           |
| crypto_pyaes             | 77.5 ms                                                    | 74.8 ms: 1.04x faster                                                          |
| mako                     | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                                          |
| sqlite_synth             | 2.99 us                                                    | 2.89 us: 1.03x faster                                                          |
| float                    | 78.9 ms                                                    | 76.4 ms: 1.03x faster                                                          |
| chameleon                | 7.22 ms                                                    | 7.00 ms: 1.03x faster                                                          |
| pprint_pformat           | 1.56 sec                                                   | 1.52 sec: 1.03x faster                                                         |
| unpickle_list            | 5.34 us                                                    | 5.21 us: 1.03x faster                                                          |
| deepcopy                 | 367 us                                                     | 360 us: 1.02x faster                                                           |
| coroutines               | 23.2 ms                                                    | 22.8 ms: 1.02x faster                                                          |
| regex_effbot             | 3.67 ms                                                    | 3.62 ms: 1.01x faster                                                          |
| pprint_safe_repr         | 758 ms                                                     | 748 ms: 1.01x faster                                                           |
| tomli_loads              | 2.12 sec                                                   | 2.09 sec: 1.01x faster                                                         |
| pickle_list              | 5.11 us                                                    | 5.04 us: 1.01x faster                                                          |
| pidigits                 | 191 ms                                                     | 189 ms: 1.01x faster                                                           |
| regex_dna                | 221 ms                                                     | 219 ms: 1.01x faster                                                           |
| spectral_norm            | 116 ms                                                     | 115 ms: 1.01x faster                                                           |
| xml_etree_process        | 61.2 ms                                                    | 60.8 ms: 1.01x faster                                                          |
| gc_traversal             | 3.98 ms                                                    | 3.95 ms: 1.01x faster                                                          |
| asyncio_tcp              | 508 ms                                                     | 506 ms: 1.00x faster                                                           |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.85 sec: 1.00x slower                                                         |
| asyncio_websockets       | 567 ms                                                     | 569 ms: 1.00x slower                                                           |
| pyflate                  | 484 ms                                                     | 488 ms: 1.01x slower                                                           |
| thrift                   | 823 us                                                     | 831 us: 1.01x slower                                                           |
| html5lib                 | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                                          |
| sqlglot_transpile        | 1.63 ms                                                    | 1.66 ms: 1.02x slower                                                          |
| sqlglot_parse            | 1.32 ms                                                    | 1.34 ms: 1.02x slower                                                          |
| generators               | 29.6 ms                                                    | 30.1 ms: 1.02x slower                                                          |
| xml_etree_generate       | 87.4 ms                                                    | 88.8 ms: 1.02x slower                                                          |
| djangocms                | 31.5 us                                                    | 32.0 us: 1.02x slower                                                          |
| json                     | 5.31 ms                                                    | 5.40 ms: 1.02x slower                                                          |
| scimark_monte_carlo      | 69.2 ms                                                    | 70.3 ms: 1.02x slower                                                          |
| regex_v8                 | 25.1 ms                                                    | 25.5 ms: 1.02x slower                                                          |
| pickle_pure_python       | 305 us                                                     | 311 us: 1.02x slower                                                           |
| 2to3                     | 274 ms                                                     | 280 ms: 1.02x slower                                                           |
| telco                    | 8.41 ms                                                    | 8.59 ms: 1.02x slower                                                          |
| docutils                 | 2.83 sec                                                   | 2.89 sec: 1.02x slower                                                         |
| tornado_http             | 94.6 ms                                                    | 96.9 ms: 1.02x slower                                                          |
| dask                     | 369 ms                                                     | 378 ms: 1.02x slower                                                           |
| meteor_contest           | 110 ms                                                     | 112 ms: 1.02x slower                                                           |
| gunicorn                 | 1.28 ms                                                    | 1.31 ms: 1.03x slower                                                          |
| logging_format           | 6.47 us                                                    | 6.64 us: 1.03x slower                                                          |
| pycparser                | 1.16 sec                                                   | 1.19 sec: 1.03x slower                                                         |
| unpickle                 | 15.1 us                                                    | 15.5 us: 1.03x slower                                                          |
| bench_thread_pool        | 834 us                                                     | 860 us: 1.03x slower                                                           |
| sqlglot_normalize        | 110 ms                                                     | 114 ms: 1.03x slower                                                           |
| sympy_str                | 282 ms                                                     | 291 ms: 1.03x slower                                                           |
| chaos                    | 61.3 ms                                                    | 63.4 ms: 1.03x slower                                                          |
| aiohttp                  | 1.18 ms                                                    | 1.22 ms: 1.03x slower                                                          |
| async_tree_none_tg       | 336 ms                                                     | 347 ms: 1.03x slower                                                           |
| pickle_dict              | 34.8 us                                                    | 36.0 us: 1.03x slower                                                          |
| python_startup           | 10.8 ms                                                    | 11.1 ms: 1.04x slower                                                          |
| django_template          | 34.8 ms                                                    | 36.0 ms: 1.04x slower                                                          |
| pickle                   | 11.5 us                                                    | 11.9 us: 1.04x slower                                                          |
| sqlglot_optimize         | 55.5 ms                                                    | 58.0 ms: 1.04x slower                                                          |
| logging_simple           | 5.74 us                                                    | 6.01 us: 1.05x slower                                                          |
| sympy_expand             | 473 ms                                                     | 495 ms: 1.05x slower                                                           |
| nbody                    | 88.3 ms                                                    | 92.5 ms: 1.05x slower                                                          |
| scimark_sor              | 127 ms                                                     | 134 ms: 1.05x slower                                                           |
| async_generators         | 442 ms                                                     | 464 ms: 1.05x slower                                                           |
| dulwich_log              | 67.2 ms                                                    | 70.7 ms: 1.05x slower                                                          |
| coverage                 | 93.1 ms                                                    | 98.1 ms: 1.05x slower                                                          |
| genshi_text              | 23.7 ms                                                    | 25.0 ms: 1.06x slower                                                          |
| mypy2                    | 742 ms                                                     | 787 ms: 1.06x slower                                                           |
| sympy_sum                | 156 ms                                                     | 166 ms: 1.06x slower                                                           |
| sympy_integrate          | 20.5 ms                                                    | 21.9 ms: 1.07x slower                                                          |
| go                       | 145 ms                                                     | 155 ms: 1.07x slower                                                           |
| regex_compile            | 137 ms                                                     | 147 ms: 1.07x slower                                                           |
| genshi_xml               | 51.6 ms                                                    | 55.8 ms: 1.08x slower                                                          |
| deltablue                | 3.25 ms                                                    | 3.53 ms: 1.09x slower                                                          |
| pathlib                  | 17.3 ms                                                    | 18.8 ms: 1.09x slower                                                          |
| scimark_lu               | 122 ms                                                     | 133 ms: 1.09x slower                                                           |
| nqueens                  | 81.4 ms                                                    | 90.2 ms: 1.11x slower                                                          |
| raytrace                 | 267 ms                                                     | 296 ms: 1.11x slower                                                           |
| comprehensions           | 16.6 us                                                    | 18.4 us: 1.11x slower                                                          |
| unpickle_pure_python     | 218 us                                                     | 245 us: 1.12x slower                                                           |
| hexiom                   | 6.30 ms                                                    | 7.29 ms: 1.16x slower                                                          |
| python_startup_no_site   | 7.11 ms                                                    | 9.56 ms: 1.35x slower                                                          |
| Geometric mean           | (ref)                                                      | 1.01x slower                                                                   |

Benchmark hidden because not significant (14): async_tree_io, json_dumps, async_tree_memoization, async_tree_cpu_io_mixed, deepcopy_memo, logging_silent, xml_etree_iterparse, xml_etree_parse, fannkuch, bench_mp_pool, async_tree_memoization_tg, json_loads, async_tree_cpu_io_mixed_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240327-3.13.0a5+-a65be06-JIT/bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06.json: unpack_sequence

# HPT report

- Reliability score: 99.83% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.05x