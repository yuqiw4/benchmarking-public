# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-amd64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.01x slower
- HPT reliability: 99.47%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 220 ms: 1.06x slower                                                        |
| chameleon      | 4.80 ms                                                         | 4.68 ms: 1.03x faster                                                       |
| docutils       | 1.63 sec                                                        | 1.69 sec: 1.04x slower                                                      |
| html5lib       | 35.0 ms                                                         | 35.2 ms: 1.01x slower                                                       |
| tornado_http   | 81.8 ms                                                         | 83.7 ms: 1.02x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|--------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_none    | 218 ms                                                          | 223 ms: 1.02x slower                                                        |
| async_tree_none_tg | 202 ms                                                          | 216 ms: 1.07x slower                                                        |
| Geometric mean     | (ref)                                                           | 1.02x slower                                                                |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 57.5 ms: 1.18x faster                                                       |
| float          | 49.7 ms                                                         | 46.6 ms: 1.07x faster                                                       |
| pidigits       | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.3 ms: 1.10x faster                                                       |
| regex_dna      | 119 ms                                                          | 116 ms: 1.03x faster                                                        |
| regex_effbot   | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                       |
| regex_compile  | 78.0 ms                                                         | 86.6 ms: 1.11x slower                                                       |
| Geometric mean | (ref)                                                           | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.21 sec: 1.12x faster                                                      |
| json_loads           | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| xml_etree_iterparse  | 62.3 ms                                                         | 60.6 ms: 1.03x faster                                                       |
| pickle_pure_python   | 175 us                                                          | 172 us: 1.02x faster                                                        |
| json_dumps           | 5.61 ms                                                         | 5.59 ms: 1.01x faster                                                       |
| xml_etree_generate   | 53.2 ms                                                         | 53.0 ms: 1.00x faster                                                       |
| xml_etree_process    | 36.4 ms                                                         | 36.8 ms: 1.01x slower                                                       |
| pickle               | 7.11 us                                                         | 7.22 us: 1.01x slower                                                       |
| pickle_list          | 2.90 us                                                         | 2.99 us: 1.03x slower                                                       |
| pickle_dict          | 18.1 us                                                         | 18.8 us: 1.04x slower                                                       |
| unpickle_list        | 2.62 us                                                         | 2.78 us: 1.06x slower                                                       |
| unpickle             | 8.40 us                                                         | 9.07 us: 1.08x slower                                                       |
| unpickle_pure_python | 122 us                                                          | 132 us: 1.09x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 21.5 ms: 1.06x slower                                                       |
| python_startup_no_site | 16.2 ms                                                         | 19.6 ms: 1.21x slower                                                       |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 6.36 ms                                                         | 5.71 ms: 1.11x faster                                                       |
| genshi_text    | 14.4 ms                                                         | 15.4 ms: 1.07x slower                                                       |
| genshi_xml     | 31.6 ms                                                         | 34.7 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240410-pythonperf1-amd64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|--------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 73.1 us: 1.38x faster                                                       |
| spectral_norm            | 63.7 ms                                                         | 51.6 ms: 1.23x faster                                                       |
| nbody                    | 67.6 ms                                                         | 57.5 ms: 1.18x faster                                                       |
| tomli_loads              | 1.35 sec                                                        | 1.21 sec: 1.12x faster                                                      |
| mako                     | 6.36 ms                                                         | 5.71 ms: 1.11x faster                                                       |
| json                     | 3.19 ms                                                         | 2.88 ms: 1.11x faster                                                       |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.26 ms: 1.11x faster                                                       |
| regex_v8                 | 15.8 ms                                                         | 14.3 ms: 1.10x faster                                                       |
| pycparser                | 754 ms                                                          | 686 ms: 1.10x faster                                                        |
| float                    | 49.7 ms                                                         | 46.6 ms: 1.07x faster                                                       |
| pylint                   | 205 ms                                                          | 195 ms: 1.05x faster                                                        |
| fannkuch                 | 243 ms                                                          | 232 ms: 1.05x faster                                                        |
| deepcopy_memo            | 22.1 us                                                         | 21.1 us: 1.05x faster                                                       |
| json_loads               | 14.2 us                                                         | 13.8 us: 1.03x faster                                                       |
| xml_etree_iterparse      | 62.3 ms                                                         | 60.6 ms: 1.03x faster                                                       |
| scimark_fft              | 171 ms                                                          | 166 ms: 1.03x faster                                                        |
| regex_dna                | 119 ms                                                          | 116 ms: 1.03x faster                                                        |
| chameleon                | 4.80 ms                                                         | 4.68 ms: 1.03x faster                                                       |
| pidigits                 | 150 ms                                                          | 147 ms: 1.02x faster                                                        |
| crypto_pyaes             | 45.5 ms                                                         | 44.5 ms: 1.02x faster                                                       |
| pprint_pformat           | 966 ms                                                          | 945 ms: 1.02x faster                                                        |
| regex_effbot             | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                       |
| scimark_monte_carlo      | 39.1 ms                                                         | 38.4 ms: 1.02x faster                                                       |
| pickle_pure_python       | 175 us                                                          | 172 us: 1.02x faster                                                        |
| pyflate                  | 279 ms                                                          | 274 ms: 1.02x faster                                                        |
| logging_format           | 6.22 us                                                         | 6.12 us: 1.02x faster                                                       |
| sqlite_synth             | 1.60 us                                                         | 1.57 us: 1.02x faster                                                       |
| deepcopy_reduce          | 1.99 us                                                         | 1.97 us: 1.01x faster                                                       |
| pathlib                  | 75.9 ms                                                         | 74.9 ms: 1.01x faster                                                       |
| logging_simple           | 5.78 us                                                         | 5.71 us: 1.01x faster                                                       |
| pprint_safe_repr         | 474 ms                                                          | 470 ms: 1.01x faster                                                        |
| json_dumps               | 5.61 ms                                                         | 5.59 ms: 1.01x faster                                                       |
| xml_etree_generate       | 53.2 ms                                                         | 53.0 ms: 1.00x faster                                                       |
| html5lib                 | 35.0 ms                                                         | 35.2 ms: 1.01x slower                                                       |
| generators               | 19.6 ms                                                         | 19.7 ms: 1.01x slower                                                       |
| telco                    | 4.67 ms                                                         | 4.71 ms: 1.01x slower                                                       |
| chaos                    | 38.4 ms                                                         | 38.7 ms: 1.01x slower                                                       |
| xml_etree_process        | 36.4 ms                                                         | 36.8 ms: 1.01x slower                                                       |
| create_gc_cycles         | 888 us                                                          | 899 us: 1.01x slower                                                        |
| pickle                   | 7.11 us                                                         | 7.22 us: 1.01x slower                                                       |
| aiohttp                  | 889 us                                                          | 902 us: 1.02x slower                                                        |
| raytrace                 | 162 ms                                                          | 165 ms: 1.02x slower                                                        |
| async_tree_none          | 218 ms                                                          | 223 ms: 1.02x slower                                                        |
| coroutines               | 12.8 ms                                                         | 13.0 ms: 1.02x slower                                                       |
| deepcopy                 | 220 us                                                          | 224 us: 1.02x slower                                                        |
| tornado_http             | 81.8 ms                                                         | 83.7 ms: 1.02x slower                                                       |
| pickle_list              | 2.90 us                                                         | 2.99 us: 1.03x slower                                                       |
| meteor_contest           | 69.9 ms                                                         | 72.3 ms: 1.03x slower                                                       |
| pickle_dict              | 18.1 us                                                         | 18.8 us: 1.04x slower                                                       |
| docutils                 | 1.63 sec                                                        | 1.69 sec: 1.04x slower                                                      |
| comprehensions           | 10.4 us                                                         | 10.8 us: 1.04x slower                                                       |
| sqlglot_parse            | 748 us                                                          | 780 us: 1.04x slower                                                        |
| bench_mp_pool            | 64.8 ms                                                         | 67.6 ms: 1.04x slower                                                       |
| sympy_expand             | 271 ms                                                          | 282 ms: 1.04x slower                                                        |
| sympy_str                | 159 ms                                                          | 167 ms: 1.05x slower                                                        |
| sqlglot_normalize        | 173 ms                                                          | 181 ms: 1.05x slower                                                        |
| sqlglot_transpile        | 955 us                                                          | 1.00 ms: 1.05x slower                                                       |
| sympy_sum                | 84.4 ms                                                         | 88.9 ms: 1.05x slower                                                       |
| bench_thread_pool        | 768 us                                                          | 811 us: 1.06x slower                                                        |
| python_startup           | 20.3 ms                                                         | 21.5 ms: 1.06x slower                                                       |
| unpickle_list            | 2.62 us                                                         | 2.78 us: 1.06x slower                                                       |
| 2to3                     | 207 ms                                                          | 220 ms: 1.06x slower                                                        |
| async_generators         | 223 ms                                                          | 238 ms: 1.07x slower                                                        |
| async_tree_none_tg       | 202 ms                                                          | 216 ms: 1.07x slower                                                        |
| thrift                   | 8.11 ms                                                         | 8.68 ms: 1.07x slower                                                       |
| sqlglot_optimize         | 32.7 ms                                                         | 35.0 ms: 1.07x slower                                                       |
| genshi_text              | 14.4 ms                                                         | 15.4 ms: 1.07x slower                                                       |
| coverage                 | 42.1 ms                                                         | 45.3 ms: 1.08x slower                                                       |
| mypy2                    | 418 ms                                                          | 450 ms: 1.08x slower                                                        |
| dulwich_log              | 38.0 ms                                                         | 41.0 ms: 1.08x slower                                                       |
| unpickle                 | 8.40 us                                                         | 9.07 us: 1.08x slower                                                       |
| unpickle_pure_python     | 122 us                                                          | 132 us: 1.09x slower                                                        |
| sympy_integrate          | 12.2 ms                                                         | 13.3 ms: 1.09x slower                                                       |
| mdp                      | 1.31 sec                                                        | 1.43 sec: 1.09x slower                                                      |
| nqueens                  | 56.7 ms                                                         | 62.0 ms: 1.09x slower                                                       |
| genshi_xml               | 31.6 ms                                                         | 34.7 ms: 1.10x slower                                                       |
| scimark_sor              | 75.3 ms                                                         | 83.0 ms: 1.10x slower                                                       |
| regex_compile            | 78.0 ms                                                         | 86.6 ms: 1.11x slower                                                       |
| go                       | 82.1 ms                                                         | 92.7 ms: 1.13x slower                                                       |
| deltablue                | 1.88 ms                                                         | 2.16 ms: 1.15x slower                                                       |
| hexiom                   | 3.72 ms                                                         | 4.41 ms: 1.18x slower                                                       |
| python_startup_no_site   | 16.2 ms                                                         | 19.6 ms: 1.21x slower                                                       |
| scimark_lu               | 56.6 ms                                                         | 71.0 ms: 1.25x slower                                                       |
| Geometric mean           | (ref)                                                           | 1.01x slower                                                                |

Benchmark hidden because not significant (13): asyncio_tcp, xml_etree_parse, async_tree_cpu_io_mixed, richards, gc_traversal, async_tree_cpu_io_mixed_tg, logging_silent, async_tree_io, richards_super, async_tree_io_tg, async_tree_memoization, asyncio_tcp_ssl, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: django_template, flaskblogging

# HPT report

- Reliability score: 99.47% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown