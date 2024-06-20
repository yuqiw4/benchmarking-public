# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_align
- machine: linux-x86_64
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                           | 299 ms: 1.03x slower                                                       |
| chameleon      | 7.40 ms                                                          | 7.12 ms: 1.04x faster                                                      |
| docutils       | 2.98 sec                                                         | 3.06 sec: 1.03x slower                                                     |
| html5lib       | 74.7 ms                                                          | 72.8 ms: 1.03x faster                                                      |
| tornado_http   | 119 ms                                                           | 125 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                            | 1.01x slower                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_memoization  | 460 ms                                                           | 441 ms: 1.04x faster                                                       |
| async_tree_none         | 365 ms                                                           | 358 ms: 1.02x faster                                                       |
| async_tree_cpu_io_mixed | 604 ms                                                           | 594 ms: 1.02x faster                                                       |
| Geometric mean          | (ref)                                                            | 1.01x faster                                                               |

Benchmark hidden because not significant (5): async_tree_none_tg, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 80.2 ms                                                          | 78.0 ms: 1.03x faster                                                      |
| pidigits       | 254 ms                                                           | 261 ms: 1.03x slower                                                       |
| nbody          | 87.8 ms                                                          | 97.3 ms: 1.11x slower                                                      |
| Geometric mean | (ref)                                                            | 1.04x slower                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_dna      | 249 ms                                                           | 238 ms: 1.05x faster                                                       |
| regex_compile  | 144 ms                                                           | 147 ms: 1.02x slower                                                       |
| regex_effbot   | 3.40 ms                                                          | 3.46 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                            | 1.00x faster                                                               |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 2.40 sec                                                         | 2.14 sec: 1.12x faster                                                     |
| unpickle             | 15.7 us                                                          | 14.8 us: 1.06x faster                                                      |
| xml_etree_generate   | 85.7 ms                                                          | 83.4 ms: 1.03x faster                                                      |
| xml_etree_process    | 59.7 ms                                                          | 58.1 ms: 1.03x faster                                                      |
| unpickle_list        | 4.70 us                                                          | 4.60 us: 1.02x faster                                                      |
| json_dumps           | 10.8 ms                                                          | 10.6 ms: 1.01x faster                                                      |
| xml_etree_parse      | 144 ms                                                           | 143 ms: 1.00x faster                                                       |
| pickle               | 10.6 us                                                          | 10.7 us: 1.01x slower                                                      |
| json_loads           | 25.0 us                                                          | 25.3 us: 1.01x slower                                                      |
| pickle_list          | 4.44 us                                                          | 4.50 us: 1.01x slower                                                      |
| pickle_dict          | 32.8 us                                                          | 33.6 us: 1.02x slower                                                      |
| pickle_pure_python   | 307 us                                                           | 315 us: 1.03x slower                                                       |
| unpickle_pure_python | 224 us                                                           | 235 us: 1.05x slower                                                       |
| Geometric mean       | (ref)                                                            | 1.01x faster                                                               |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                      |
| python_startup_no_site | 8.85 ms                                                          | 11.7 ms: 1.32x slower                                                      |
| Geometric mean         | (ref)                                                            | 1.16x slower                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako           | 10.4 ms                                                          | 9.91 ms: 1.05x faster                                                      |
| genshi_text    | 25.9 ms                                                          | 26.6 ms: 1.03x slower                                                      |
| Geometric mean | (ref)                                                            | 1.00x faster                                                               |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|--------------------------|:----------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols | 171 us                                                           | 117 us: 1.46x faster                                                       |
| tomli_loads              | 2.40 sec                                                         | 2.14 sec: 1.12x faster                                                     |
| create_gc_cycles         | 2.00 ms                                                          | 1.79 ms: 1.12x faster                                                      |
| unpickle                 | 15.7 us                                                          | 14.8 us: 1.06x faster                                                      |
| richards_super           | 61.2 ms                                                          | 57.8 ms: 1.06x faster                                                      |
| richards                 | 53.4 ms                                                          | 50.9 ms: 1.05x faster                                                      |
| sqlite_synth             | 2.80 us                                                          | 2.67 us: 1.05x faster                                                      |
| regex_dna                | 249 ms                                                           | 238 ms: 1.05x faster                                                       |
| mako                     | 10.4 ms                                                          | 9.91 ms: 1.05x faster                                                      |
| async_tree_memoization   | 460 ms                                                           | 441 ms: 1.04x faster                                                       |
| spectral_norm            | 97.3 ms                                                          | 93.5 ms: 1.04x faster                                                      |
| chameleon                | 7.40 ms                                                          | 7.12 ms: 1.04x faster                                                      |
| scimark_sparse_mat_mult  | 4.28 ms                                                          | 4.14 ms: 1.04x faster                                                      |
| telco                    | 8.40 ms                                                          | 8.14 ms: 1.03x faster                                                      |
| gc_traversal             | 4.69 ms                                                          | 4.55 ms: 1.03x faster                                                      |
| xml_etree_generate       | 85.7 ms                                                          | 83.4 ms: 1.03x faster                                                      |
| float                    | 80.2 ms                                                          | 78.0 ms: 1.03x faster                                                      |
| xml_etree_process        | 59.7 ms                                                          | 58.1 ms: 1.03x faster                                                      |
| asyncio_tcp              | 378 ms                                                           | 368 ms: 1.03x faster                                                       |
| html5lib                 | 74.7 ms                                                          | 72.8 ms: 1.03x faster                                                      |
| async_tree_none          | 365 ms                                                           | 358 ms: 1.02x faster                                                       |
| unpickle_list            | 4.70 us                                                          | 4.60 us: 1.02x faster                                                      |
| async_tree_cpu_io_mixed  | 604 ms                                                           | 594 ms: 1.02x faster                                                       |
| json_dumps               | 10.8 ms                                                          | 10.6 ms: 1.01x faster                                                      |
| asyncio_websockets       | 395 ms                                                           | 391 ms: 1.01x faster                                                       |
| thrift                   | 880 us                                                           | 873 us: 1.01x faster                                                       |
| xml_etree_parse          | 144 ms                                                           | 143 ms: 1.00x faster                                                       |
| asyncio_tcp_ssl          | 1.58 sec                                                         | 1.58 sec: 1.00x faster                                                     |
| deepcopy_memo            | 37.3 us                                                          | 37.4 us: 1.00x slower                                                      |
| json                     | 5.35 ms                                                          | 5.39 ms: 1.01x slower                                                      |
| pickle                   | 10.6 us                                                          | 10.7 us: 1.01x slower                                                      |
| json_loads               | 25.0 us                                                          | 25.3 us: 1.01x slower                                                      |
| logging_format           | 7.11 us                                                          | 7.19 us: 1.01x slower                                                      |
| pickle_list              | 4.44 us                                                          | 4.50 us: 1.01x slower                                                      |
| sqlglot_normalize        | 120 ms                                                           | 122 ms: 1.01x slower                                                       |
| pprint_safe_repr         | 818 ms                                                           | 831 ms: 1.02x slower                                                       |
| regex_compile            | 144 ms                                                           | 147 ms: 1.02x slower                                                       |
| regex_effbot             | 3.40 ms                                                          | 3.46 ms: 1.02x slower                                                      |
| python_startup           | 13.2 ms                                                          | 13.5 ms: 1.02x slower                                                      |
| sympy_expand             | 501 ms                                                           | 512 ms: 1.02x slower                                                       |
| generators               | 33.5 ms                                                          | 34.3 ms: 1.02x slower                                                      |
| sympy_str                | 295 ms                                                           | 301 ms: 1.02x slower                                                       |
| dulwich_log              | 67.3 ms                                                          | 68.9 ms: 1.02x slower                                                      |
| pickle_dict              | 32.8 us                                                          | 33.6 us: 1.02x slower                                                      |
| pickle_pure_python       | 307 us                                                           | 315 us: 1.03x slower                                                       |
| 2to3                     | 291 ms                                                           | 299 ms: 1.03x slower                                                       |
| logging_silent           | 96.3 ns                                                          | 98.8 ns: 1.03x slower                                                      |
| docutils                 | 2.98 sec                                                         | 3.06 sec: 1.03x slower                                                     |
| genshi_text              | 25.9 ms                                                          | 26.6 ms: 1.03x slower                                                      |
| meteor_contest           | 128 ms                                                           | 132 ms: 1.03x slower                                                       |
| pyflate                  | 482 ms                                                           | 496 ms: 1.03x slower                                                       |
| pycparser                | 1.22 sec                                                         | 1.26 sec: 1.03x slower                                                     |
| pidigits                 | 254 ms                                                           | 261 ms: 1.03x slower                                                       |
| logging_simple           | 6.40 us                                                          | 6.60 us: 1.03x slower                                                      |
| coverage                 | 83.5 ms                                                          | 86.2 ms: 1.03x slower                                                      |
| scimark_fft              | 312 ms                                                           | 322 ms: 1.03x slower                                                       |
| dask                     | 391 ms                                                           | 404 ms: 1.03x slower                                                       |
| gunicorn                 | 1.04 ms                                                          | 1.08 ms: 1.04x slower                                                      |
| sqlglot_parse            | 1.39 ms                                                          | 1.44 ms: 1.04x slower                                                      |
| sqlglot_transpile        | 1.76 ms                                                          | 1.83 ms: 1.04x slower                                                      |
| pprint_pformat           | 1.66 sec                                                         | 1.73 sec: 1.04x slower                                                     |
| tornado_http             | 119 ms                                                           | 125 ms: 1.04x slower                                                       |
| sympy_sum                | 155 ms                                                           | 162 ms: 1.04x slower                                                       |
| unpickle_pure_python     | 224 us                                                           | 235 us: 1.05x slower                                                       |
| go                       | 165 ms                                                           | 173 ms: 1.05x slower                                                       |
| sqlglot_optimize         | 59.5 ms                                                          | 62.8 ms: 1.06x slower                                                      |
| aiohttp                  | 1.07 ms                                                          | 1.13 ms: 1.06x slower                                                      |
| crypto_pyaes             | 73.6 ms                                                          | 78.2 ms: 1.06x slower                                                      |
| mdp                      | 2.46 sec                                                         | 2.62 sec: 1.06x slower                                                     |
| fannkuch                 | 353 ms                                                           | 378 ms: 1.07x slower                                                       |
| coroutines               | 22.0 ms                                                          | 23.7 ms: 1.08x slower                                                      |
| async_generators         | 363 ms                                                           | 392 ms: 1.08x slower                                                       |
| sympy_integrate          | 23.2 ms                                                          | 25.1 ms: 1.08x slower                                                      |
| mypy2                    | 764 ms                                                           | 828 ms: 1.08x slower                                                       |
| deltablue                | 3.37 ms                                                          | 3.71 ms: 1.10x slower                                                      |
| nbody                    | 87.8 ms                                                          | 97.3 ms: 1.11x slower                                                      |
| pathlib                  | 17.1 ms                                                          | 19.1 ms: 1.12x slower                                                      |
| chaos                    | 59.6 ms                                                          | 66.8 ms: 1.12x slower                                                      |
| scimark_monte_carlo      | 65.5 ms                                                          | 74.6 ms: 1.14x slower                                                      |
| comprehensions           | 17.0 us                                                          | 19.9 us: 1.17x slower                                                      |
| hexiom                   | 6.35 ms                                                          | 7.53 ms: 1.19x slower                                                      |
| raytrace                 | 260 ms                                                           | 310 ms: 1.19x slower                                                       |
| nqueens                  | 88.4 ms                                                          | 105 ms: 1.19x slower                                                       |
| bench_thread_pool        | 908 us                                                           | 1.12 ms: 1.24x slower                                                      |
| scimark_lu               | 97.5 ms                                                          | 122 ms: 1.25x slower                                                       |
| scimark_sor              | 119 ms                                                           | 153 ms: 1.29x slower                                                       |
| python_startup_no_site   | 8.85 ms                                                          | 11.7 ms: 1.32x slower                                                      |
| Geometric mean           | (ref)                                                            | 1.03x slower                                                               |

Benchmark hidden because not significant (13): async_tree_none_tg, pylint, deepcopy_reduce, genshi_xml, xml_etree_iterparse, deepcopy, django_template, async_tree_io_tg, async_tree_cpu_io_mixed_tg, regex_v8, async_tree_io, async_tree_memoization_tg, bench_mp_pool
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-d1a7b3a-JIT/bm-20240330-pythonperf2-x86_64-brandtbucher-justin_align-3.13.0a5+-d1a7b3a.json: unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.06x