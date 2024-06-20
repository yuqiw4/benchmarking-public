# Results vs. 3.13.0b2

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: f6bf194
- commit date: 2024-03-26
- overall geometric mean: 1.01x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-f6bf194 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 279 ms: 1.02x slower                                              |
| chameleon      | 7.22 ms                                                    | 7.17 ms: 1.01x faster                                             |
| html5lib       | 67.2 ms                                                    | 66.2 ms: 1.02x faster                                             |
| tornado_http   | 94.6 ms                                                    | 96.5 ms: 1.02x slower                                             |
| Geometric mean | (ref)                                                      | 1.00x slower                                                      |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-f6bf194 |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none | 378 ms                                                     | 386 ms: 1.02x slower                                              |
| Geometric mean  | (ref)                                                      | 1.00x faster                                                      |

Benchmark hidden because not significant (7): async_tree_io, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-f6bf194 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 77.5 ms: 1.02x faster                                             |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                              |
| nbody          | 88.3 ms                                                    | 92.2 ms: 1.04x slower                                             |
| Geometric mean | (ref)                                                      | 1.00x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-f6bf194 |
|----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 137 ms                                                     | 139 ms: 1.01x slower                                              |
| regex_v8       | 25.1 ms                                                    | 25.7 ms: 1.02x slower                                             |
| regex_effbot   | 3.67 ms                                                    | 3.77 ms: 1.03x slower                                             |
| regex_dna      | 221 ms                                                     | 227 ms: 1.03x slower                                              |
| Geometric mean | (ref)                                                      | 1.02x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-f6bf194 |
|----------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_dict          | 34.8 us                                                    | 33.5 us: 1.04x faster                                             |
| pickle_list          | 5.11 us                                                    | 4.95 us: 1.03x faster                                             |
| tomli_loads          | 2.12 sec                                                   | 2.06 sec: 1.03x faster                                            |
| xml_etree_process    | 61.2 ms                                                    | 60.1 ms: 1.02x faster                                             |
| json_dumps           | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                             |
| xml_etree_generate   | 87.4 ms                                                    | 86.9 ms: 1.01x faster                                             |
| unpickle_list        | 5.34 us                                                    | 5.43 us: 1.02x slower                                             |
| pickle               | 11.5 us                                                    | 12.0 us: 1.05x slower                                             |
| unpickle_pure_python | 218 us                                                     | 232 us: 1.06x slower                                              |
| unpickle             | 15.1 us                                                    | 17.0 us: 1.12x slower                                             |
| Geometric mean       | (ref)                                                      | 1.01x slower                                                      |

Benchmark hidden because not significant (4): json_loads, xml_etree_parse, xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-f6bf194 |
|------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                             |
| python_startup_no_site | 7.11 ms                                                    | 9.48 ms: 1.33x slower                                             |
| Geometric mean         | (ref)                                                      | 1.17x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-f6bf194 |
|-----------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                             |
| django_template | 34.8 ms                                                    | 35.8 ms: 1.03x slower                                             |
| genshi_xml      | 51.6 ms                                                    | 54.1 ms: 1.05x slower                                             |
| genshi_text     | 23.7 ms                                                    | 25.2 ms: 1.07x slower                                             |
| Geometric mean  | (ref)                                                      | 1.03x slower                                                      |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240326-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-f6bf194 |
|--------------------------|:----------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 114 us: 1.45x faster                                              |
| richards                 | 50.9 ms                                                    | 44.1 ms: 1.15x faster                                             |
| scimark_fft              | 392 ms                                                     | 344 ms: 1.14x faster                                              |
| richards_super           | 57.4 ms                                                    | 50.7 ms: 1.13x faster                                             |
| create_gc_cycles         | 1.82 ms                                                    | 1.69 ms: 1.08x faster                                             |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.93 ms: 1.07x faster                                             |
| deepcopy_reduce          | 3.35 us                                                    | 3.15 us: 1.06x faster                                             |
| scimark_lu               | 122 ms                                                     | 115 ms: 1.06x faster                                              |
| mdp                      | 2.79 sec                                                   | 2.66 sec: 1.05x faster                                            |
| pickle_dict              | 34.8 us                                                    | 33.5 us: 1.04x faster                                             |
| sqlite_synth             | 2.99 us                                                    | 2.89 us: 1.04x faster                                             |
| mako                     | 11.2 ms                                                    | 10.9 ms: 1.03x faster                                             |
| pickle_list              | 5.11 us                                                    | 4.95 us: 1.03x faster                                             |
| gc_traversal             | 3.98 ms                                                    | 3.86 ms: 1.03x faster                                             |
| tomli_loads              | 2.12 sec                                                   | 2.06 sec: 1.03x faster                                            |
| crypto_pyaes             | 77.5 ms                                                    | 75.5 ms: 1.03x faster                                             |
| scimark_sor              | 127 ms                                                     | 124 ms: 1.02x faster                                              |
| deepcopy                 | 367 us                                                     | 359 us: 1.02x faster                                              |
| xml_etree_process        | 61.2 ms                                                    | 60.1 ms: 1.02x faster                                             |
| float                    | 78.9 ms                                                    | 77.5 ms: 1.02x faster                                             |
| deepcopy_memo            | 39.7 us                                                    | 39.0 us: 1.02x faster                                             |
| html5lib                 | 67.2 ms                                                    | 66.2 ms: 1.02x faster                                             |
| json_dumps               | 10.7 ms                                                    | 10.6 ms: 1.01x faster                                             |
| pidigits                 | 191 ms                                                     | 189 ms: 1.01x faster                                              |
| chameleon                | 7.22 ms                                                    | 7.17 ms: 1.01x faster                                             |
| xml_etree_generate       | 87.4 ms                                                    | 86.9 ms: 1.01x faster                                             |
| asyncio_tcp              | 508 ms                                                     | 506 ms: 1.00x faster                                              |
| pyflate                  | 484 ms                                                     | 486 ms: 1.00x slower                                              |
| asyncio_websockets       | 567 ms                                                     | 570 ms: 1.01x slower                                              |
| pprint_pformat           | 1.56 sec                                                   | 1.57 sec: 1.01x slower                                            |
| bench_mp_pool            | 23.9 ms                                                    | 24.0 ms: 1.01x slower                                             |
| sqlglot_parse            | 1.32 ms                                                    | 1.33 ms: 1.01x slower                                             |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.85 sec: 1.01x slower                                            |
| sqlglot_transpile        | 1.63 ms                                                    | 1.65 ms: 1.01x slower                                             |
| meteor_contest           | 110 ms                                                     | 111 ms: 1.01x slower                                              |
| regex_compile            | 137 ms                                                     | 139 ms: 1.01x slower                                              |
| unpickle_list            | 5.34 us                                                    | 5.43 us: 1.02x slower                                             |
| 2to3                     | 274 ms                                                     | 279 ms: 1.02x slower                                              |
| coroutines               | 23.2 ms                                                    | 23.6 ms: 1.02x slower                                             |
| dask                     | 369 ms                                                     | 376 ms: 1.02x slower                                              |
| sqlglot_normalize        | 110 ms                                                     | 112 ms: 1.02x slower                                              |
| tornado_http             | 94.6 ms                                                    | 96.5 ms: 1.02x slower                                             |
| telco                    | 8.41 ms                                                    | 8.58 ms: 1.02x slower                                             |
| gunicorn                 | 1.28 ms                                                    | 1.30 ms: 1.02x slower                                             |
| deltablue                | 3.25 ms                                                    | 3.32 ms: 1.02x slower                                             |
| djangocms                | 31.5 us                                                    | 32.2 us: 1.02x slower                                             |
| async_tree_none          | 378 ms                                                     | 386 ms: 1.02x slower                                              |
| bench_thread_pool        | 834 us                                                     | 852 us: 1.02x slower                                              |
| dulwich_log              | 67.2 ms                                                    | 68.6 ms: 1.02x slower                                             |
| sqlglot_optimize         | 55.5 ms                                                    | 56.7 ms: 1.02x slower                                             |
| python_startup           | 10.8 ms                                                    | 11.0 ms: 1.02x slower                                             |
| json                     | 5.31 ms                                                    | 5.42 ms: 1.02x slower                                             |
| go                       | 145 ms                                                     | 148 ms: 1.02x slower                                              |
| generators               | 29.6 ms                                                    | 30.3 ms: 1.02x slower                                             |
| regex_v8                 | 25.1 ms                                                    | 25.7 ms: 1.02x slower                                             |
| sympy_str                | 282 ms                                                     | 289 ms: 1.02x slower                                              |
| aiohttp                  | 1.18 ms                                                    | 1.21 ms: 1.03x slower                                             |
| regex_effbot             | 3.67 ms                                                    | 3.77 ms: 1.03x slower                                             |
| django_template          | 34.8 ms                                                    | 35.8 ms: 1.03x slower                                             |
| regex_dna                | 221 ms                                                     | 227 ms: 1.03x slower                                              |
| logging_format           | 6.47 us                                                    | 6.66 us: 1.03x slower                                             |
| scimark_monte_carlo      | 69.2 ms                                                    | 71.3 ms: 1.03x slower                                             |
| chaos                    | 61.3 ms                                                    | 63.3 ms: 1.03x slower                                             |
| mypy2                    | 742 ms                                                     | 766 ms: 1.03x slower                                              |
| raytrace                 | 267 ms                                                     | 275 ms: 1.03x slower                                              |
| sympy_expand             | 473 ms                                                     | 491 ms: 1.04x slower                                              |
| sympy_integrate          | 20.5 ms                                                    | 21.3 ms: 1.04x slower                                             |
| thrift                   | 823 us                                                     | 858 us: 1.04x slower                                              |
| nbody                    | 88.3 ms                                                    | 92.2 ms: 1.04x slower                                             |
| sympy_sum                | 156 ms                                                     | 163 ms: 1.05x slower                                              |
| logging_simple           | 5.74 us                                                    | 6.02 us: 1.05x slower                                             |
| genshi_xml               | 51.6 ms                                                    | 54.1 ms: 1.05x slower                                             |
| pickle                   | 11.5 us                                                    | 12.0 us: 1.05x slower                                             |
| async_generators         | 442 ms                                                     | 468 ms: 1.06x slower                                              |
| unpickle_pure_python     | 218 us                                                     | 232 us: 1.06x slower                                              |
| genshi_text              | 23.7 ms                                                    | 25.2 ms: 1.07x slower                                             |
| pycparser                | 1.16 sec                                                   | 1.24 sec: 1.07x slower                                            |
| coverage                 | 93.1 ms                                                    | 100 ms: 1.08x slower                                              |
| nqueens                  | 81.4 ms                                                    | 87.9 ms: 1.08x slower                                             |
| comprehensions           | 16.6 us                                                    | 18.0 us: 1.08x slower                                             |
| hexiom                   | 6.30 ms                                                    | 6.87 ms: 1.09x slower                                             |
| pathlib                  | 17.3 ms                                                    | 18.9 ms: 1.09x slower                                             |
| unpickle                 | 15.1 us                                                    | 17.0 us: 1.12x slower                                             |
| python_startup_no_site   | 7.11 ms                                                    | 9.48 ms: 1.33x slower                                             |
| Geometric mean           | (ref)                                                      | 1.01x slower                                                      |

Benchmark hidden because not significant (17): async_tree_io, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg, json_loads, xml_etree_parse, xml_etree_iterparse, fannkuch, pickle_pure_python, spectral_norm, logging_silent, docutils, pprint_safe_repr, async_tree_memoization_tg, async_tree_none_tg, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240326-3.13.0a5+-f6bf194-JIT/bm-20240326-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-f6bf194.json: unpack_sequence

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.04x