# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-amd64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.02x slower
- HPT reliability: 99.65%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 222 ms: 1.07x slower                                                          |
| docutils       | 1.63 sec                                                        | 1.72 sec: 1.06x slower                                                        |
| html5lib       | 35.0 ms                                                         | 35.6 ms: 1.02x slower                                                         |
| tornado_http   | 81.8 ms                                                         | 83.6 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                           | 1.03x slower                                                                  |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg | 202 ms                                                          | 215 ms: 1.06x slower                                                          |
| Geometric mean     | (ref)                                                           | 1.02x slower                                                                  |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_memoization, async_tree_none, async_tree_io_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 59.0 ms: 1.15x faster                                                         |
| float          | 49.7 ms                                                         | 46.6 ms: 1.07x faster                                                         |
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                          |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.4 ms: 1.09x faster                                                         |
| regex_dna      | 119 ms                                                          | 116 ms: 1.02x faster                                                          |
| regex_effbot   | 1.58 ms                                                         | 1.56 ms: 1.02x faster                                                         |
| regex_compile  | 78.0 ms                                                         | 86.6 ms: 1.11x slower                                                         |
| Geometric mean | (ref)                                                           | 1.01x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.21 sec: 1.11x faster                                                        |
| json_loads           | 14.2 us                                                         | 13.6 us: 1.04x faster                                                         |
| xml_etree_iterparse  | 62.3 ms                                                         | 61.3 ms: 1.02x faster                                                         |
| json_dumps           | 5.61 ms                                                         | 5.53 ms: 1.02x faster                                                         |
| pickle_pure_python   | 175 us                                                          | 173 us: 1.01x faster                                                          |
| xml_etree_parse      | 90.9 ms                                                         | 90.3 ms: 1.01x faster                                                         |
| unpickle             | 8.40 us                                                         | 8.55 us: 1.02x slower                                                         |
| pickle_dict          | 18.1 us                                                         | 18.5 us: 1.02x slower                                                         |
| pickle               | 7.11 us                                                         | 7.29 us: 1.02x slower                                                         |
| unpickle_pure_python | 122 us                                                          | 129 us: 1.06x slower                                                          |
| unpickle_list        | 2.62 us                                                         | 2.82 us: 1.08x slower                                                         |
| pickle_list          | 2.90 us                                                         | 3.16 us: 1.09x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.01x slower                                                                  |

Benchmark hidden because not significant (2): xml_etree_generate, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 21.9 ms: 1.08x slower                                                         |
| python_startup_no_site | 16.2 ms                                                         | 19.7 ms: 1.21x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 5.64 ms: 1.13x faster                                                         |
| genshi_text    | 14.4 ms                                                         | 15.4 ms: 1.07x slower                                                         |
| genshi_xml     | 31.6 ms                                                         | 35.7 ms: 1.13x slower                                                         |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 75.2 us: 1.34x faster                                                         |
| spectral_norm            | 63.7 ms                                                         | 51.9 ms: 1.23x faster                                                         |
| nbody                    | 67.6 ms                                                         | 59.0 ms: 1.15x faster                                                         |
| mako                     | 6.36 ms                                                         | 5.64 ms: 1.13x faster                                                         |
| tomli_loads              | 1.35 sec                                                        | 1.21 sec: 1.11x faster                                                        |
| pycparser                | 754 ms                                                          | 677 ms: 1.11x faster                                                          |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.26 ms: 1.11x faster                                                         |
| json                     | 3.19 ms                                                         | 2.89 ms: 1.10x faster                                                         |
| regex_v8                 | 15.8 ms                                                         | 14.4 ms: 1.09x faster                                                         |
| float                    | 49.7 ms                                                         | 46.6 ms: 1.07x faster                                                         |
| fannkuch                 | 243 ms                                                          | 230 ms: 1.06x faster                                                          |
| json_loads               | 14.2 us                                                         | 13.6 us: 1.04x faster                                                         |
| pyflate                  | 279 ms                                                          | 270 ms: 1.03x faster                                                          |
| pidigits                 | 150 ms                                                          | 147 ms: 1.02x faster                                                          |
| sqlite_synth             | 1.60 us                                                         | 1.56 us: 1.02x faster                                                         |
| scimark_fft              | 171 ms                                                          | 167 ms: 1.02x faster                                                          |
| crypto_pyaes             | 45.5 ms                                                         | 44.5 ms: 1.02x faster                                                         |
| regex_dna                | 119 ms                                                          | 116 ms: 1.02x faster                                                          |
| regex_effbot             | 1.58 ms                                                         | 1.56 ms: 1.02x faster                                                         |
| xml_etree_iterparse      | 62.3 ms                                                         | 61.3 ms: 1.02x faster                                                         |
| json_dumps               | 5.61 ms                                                         | 5.53 ms: 1.02x faster                                                         |
| pprint_pformat           | 966 ms                                                          | 952 ms: 1.01x faster                                                          |
| deepcopy_reduce          | 1.99 us                                                         | 1.97 us: 1.01x faster                                                         |
| generators               | 19.6 ms                                                         | 19.3 ms: 1.01x faster                                                         |
| pickle_pure_python       | 175 us                                                          | 173 us: 1.01x faster                                                          |
| gc_traversal             | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                         |
| richards                 | 26.7 ms                                                         | 26.5 ms: 1.01x faster                                                         |
| richards_super           | 30.2 ms                                                         | 29.9 ms: 1.01x faster                                                         |
| xml_etree_parse          | 90.9 ms                                                         | 90.3 ms: 1.01x faster                                                         |
| pprint_safe_repr         | 474 ms                                                          | 471 ms: 1.01x faster                                                          |
| logging_format           | 6.22 us                                                         | 6.27 us: 1.01x slower                                                         |
| coroutines               | 12.8 ms                                                         | 12.9 ms: 1.01x slower                                                         |
| logging_simple           | 5.78 us                                                         | 5.86 us: 1.01x slower                                                         |
| scimark_monte_carlo      | 39.1 ms                                                         | 39.7 ms: 1.02x slower                                                         |
| html5lib                 | 35.0 ms                                                         | 35.6 ms: 1.02x slower                                                         |
| unpickle                 | 8.40 us                                                         | 8.55 us: 1.02x slower                                                         |
| pickle_dict              | 18.1 us                                                         | 18.5 us: 1.02x slower                                                         |
| telco                    | 4.67 ms                                                         | 4.76 ms: 1.02x slower                                                         |
| tornado_http             | 81.8 ms                                                         | 83.6 ms: 1.02x slower                                                         |
| pickle                   | 7.11 us                                                         | 7.29 us: 1.02x slower                                                         |
| aiohttp                  | 889 us                                                          | 911 us: 1.03x slower                                                          |
| pathlib                  | 75.9 ms                                                         | 77.9 ms: 1.03x slower                                                         |
| raytrace                 | 162 ms                                                          | 167 ms: 1.03x slower                                                          |
| sqlglot_parse            | 748 us                                                          | 774 us: 1.03x slower                                                          |
| chaos                    | 38.4 ms                                                         | 40.0 ms: 1.04x slower                                                         |
| deepcopy                 | 220 us                                                          | 229 us: 1.04x slower                                                          |
| sqlglot_transpile        | 955 us                                                          | 997 us: 1.04x slower                                                          |
| bench_mp_pool            | 64.8 ms                                                         | 67.7 ms: 1.05x slower                                                         |
| bench_thread_pool        | 768 us                                                          | 803 us: 1.05x slower                                                          |
| unpickle_pure_python     | 122 us                                                          | 129 us: 1.06x slower                                                          |
| docutils                 | 1.63 sec                                                        | 1.72 sec: 1.06x slower                                                        |
| async_tree_none_tg       | 202 ms                                                          | 215 ms: 1.06x slower                                                          |
| genshi_text              | 14.4 ms                                                         | 15.4 ms: 1.07x slower                                                         |
| sqlglot_normalize        | 173 ms                                                          | 186 ms: 1.07x slower                                                          |
| 2to3                     | 207 ms                                                          | 222 ms: 1.07x slower                                                          |
| scimark_sor              | 75.3 ms                                                         | 80.9 ms: 1.07x slower                                                         |
| python_startup           | 20.3 ms                                                         | 21.9 ms: 1.08x slower                                                         |
| sympy_sum                | 84.4 ms                                                         | 90.9 ms: 1.08x slower                                                         |
| unpickle_list            | 2.62 us                                                         | 2.82 us: 1.08x slower                                                         |
| sympy_str                | 159 ms                                                          | 172 ms: 1.08x slower                                                          |
| sympy_expand             | 271 ms                                                          | 293 ms: 1.08x slower                                                          |
| dulwich_log              | 38.0 ms                                                         | 41.2 ms: 1.08x slower                                                         |
| pickle_list              | 2.90 us                                                         | 3.16 us: 1.09x slower                                                         |
| meteor_contest           | 69.9 ms                                                         | 76.1 ms: 1.09x slower                                                         |
| comprehensions           | 10.4 us                                                         | 11.3 us: 1.09x slower                                                         |
| async_generators         | 223 ms                                                          | 243 ms: 1.09x slower                                                          |
| go                       | 82.1 ms                                                         | 89.9 ms: 1.10x slower                                                         |
| sqlglot_optimize         | 32.7 ms                                                         | 36.0 ms: 1.10x slower                                                         |
| regex_compile            | 78.0 ms                                                         | 86.6 ms: 1.11x slower                                                         |
| mypy2                    | 418 ms                                                          | 467 ms: 1.12x slower                                                          |
| nqueens                  | 56.7 ms                                                         | 63.3 ms: 1.12x slower                                                         |
| sympy_integrate          | 12.2 ms                                                         | 13.8 ms: 1.13x slower                                                         |
| coverage                 | 42.1 ms                                                         | 47.5 ms: 1.13x slower                                                         |
| genshi_xml               | 31.6 ms                                                         | 35.7 ms: 1.13x slower                                                         |
| thrift                   | 8.11 ms                                                         | 9.17 ms: 1.13x slower                                                         |
| deltablue                | 1.88 ms                                                         | 2.15 ms: 1.14x slower                                                         |
| mdp                      | 1.31 sec                                                        | 1.53 sec: 1.17x slower                                                        |
| python_startup_no_site   | 16.2 ms                                                         | 19.7 ms: 1.21x slower                                                         |
| scimark_lu               | 56.6 ms                                                         | 70.7 ms: 1.25x slower                                                         |
| hexiom                   | 3.72 ms                                                         | 4.81 ms: 1.29x slower                                                         |
| Geometric mean           | (ref)                                                           | 1.02x slower                                                                  |

Benchmark hidden because not significant (16): pylint, async_tree_cpu_io_mixed, deepcopy_memo, xml_etree_generate, async_tree_cpu_io_mixed_tg, chameleon, async_tree_io, logging_silent, asyncio_tcp_ssl, create_gc_cycles, xml_etree_process, async_tree_memoization, async_tree_none, async_tree_io_tg, asyncio_tcp, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 99.65% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown