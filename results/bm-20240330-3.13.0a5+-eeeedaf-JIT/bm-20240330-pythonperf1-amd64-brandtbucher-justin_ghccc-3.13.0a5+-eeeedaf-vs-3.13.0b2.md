# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc
- machine: windows-amd64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.01x slower
- HPT reliability: 97.98%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 207 ms                                                          | 218 ms: 1.05x slower                                                      |
| docutils       | 1.63 sec                                                        | 1.69 sec: 1.04x slower                                                    |
| html5lib       | 35.0 ms                                                         | 36.5 ms: 1.04x slower                                                     |
| tornado_http   | 81.8 ms                                                         | 85.5 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                           | 1.04x slower                                                              |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io           | 588 ms                                                          | 567 ms: 1.04x faster                                                      |
| async_tree_cpu_io_mixed | 389 ms                                                          | 376 ms: 1.04x faster                                                      |
| async_tree_io_tg        | 605 ms                                                          | 619 ms: 1.02x slower                                                      |
| Geometric mean          | (ref)                                                           | 1.00x faster                                                              |

Benchmark hidden because not significant (5): async_tree_none, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 67.6 ms                                                         | 58.3 ms: 1.16x faster                                                     |
| float          | 49.7 ms                                                         | 46.0 ms: 1.08x faster                                                     |
| pidigits       | 150 ms                                                          | 146 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                           | 1.09x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_v8       | 15.8 ms                                                         | 14.6 ms: 1.08x faster                                                     |
| regex_dna      | 119 ms                                                          | 116 ms: 1.03x faster                                                      |
| regex_effbot   | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                     |
| regex_compile  | 78.0 ms                                                         | 83.8 ms: 1.07x slower                                                     |
| Geometric mean | (ref)                                                           | 1.01x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 1.35 sec                                                        | 1.17 sec: 1.16x faster                                                    |
| xml_etree_iterparse  | 62.3 ms                                                         | 60.7 ms: 1.03x faster                                                     |
| pickle_pure_python   | 175 us                                                          | 173 us: 1.01x faster                                                      |
| json_loads           | 14.2 us                                                         | 14.0 us: 1.01x faster                                                     |
| json_dumps           | 5.61 ms                                                         | 5.55 ms: 1.01x faster                                                     |
| xml_etree_parse      | 90.9 ms                                                         | 90.1 ms: 1.01x faster                                                     |
| unpickle             | 8.40 us                                                         | 8.50 us: 1.01x slower                                                     |
| xml_etree_process    | 36.4 ms                                                         | 37.1 ms: 1.02x slower                                                     |
| pickle_dict          | 18.1 us                                                         | 18.5 us: 1.02x slower                                                     |
| pickle               | 7.11 us                                                         | 7.26 us: 1.02x slower                                                     |
| unpickle_pure_python | 122 us                                                          | 125 us: 1.03x slower                                                      |
| unpickle_list        | 2.62 us                                                         | 2.77 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                           | 1.01x faster                                                              |

Benchmark hidden because not significant (2): pickle_list, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 20.3 ms                                                         | 22.0 ms: 1.08x slower                                                     |
| python_startup_no_site | 16.2 ms                                                         | 19.6 ms: 1.21x slower                                                     |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako            | 6.36 ms                                                         | 5.22 ms: 1.22x faster                                                     |
| genshi_text     | 14.4 ms                                                         | 15.1 ms: 1.05x slower                                                     |
| django_template | 21.7 ms                                                         | 23.3 ms: 1.08x slower                                                     |
| genshi_xml      | 31.6 ms                                                         | 34.0 ms: 1.08x slower                                                     |
| Geometric mean  | (ref)                                                           | 1.00x faster                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|--------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols | 101 us                                                          | 70.2 us: 1.44x faster                                                     |
| spectral_norm            | 63.7 ms                                                         | 46.1 ms: 1.38x faster                                                     |
| mako                     | 6.36 ms                                                         | 5.22 ms: 1.22x faster                                                     |
| nbody                    | 67.6 ms                                                         | 58.3 ms: 1.16x faster                                                     |
| tomli_loads              | 1.35 sec                                                        | 1.17 sec: 1.16x faster                                                    |
| scimark_sparse_mat_mult  | 2.50 ms                                                         | 2.19 ms: 1.14x faster                                                     |
| scimark_fft              | 171 ms                                                          | 153 ms: 1.12x faster                                                      |
| fannkuch                 | 243 ms                                                          | 220 ms: 1.11x faster                                                      |
| crypto_pyaes             | 45.5 ms                                                         | 41.9 ms: 1.09x faster                                                     |
| regex_v8                 | 15.8 ms                                                         | 14.6 ms: 1.08x faster                                                     |
| scimark_monte_carlo      | 39.1 ms                                                         | 36.1 ms: 1.08x faster                                                     |
| float                    | 49.7 ms                                                         | 46.0 ms: 1.08x faster                                                     |
| json                     | 3.19 ms                                                         | 3.01 ms: 1.06x faster                                                     |
| pyflate                  | 279 ms                                                          | 264 ms: 1.06x faster                                                      |
| pylint                   | 205 ms                                                          | 195 ms: 1.05x faster                                                      |
| create_gc_cycles         | 888 us                                                          | 850 us: 1.04x faster                                                      |
| async_tree_io            | 588 ms                                                          | 567 ms: 1.04x faster                                                      |
| async_tree_cpu_io_mixed  | 389 ms                                                          | 376 ms: 1.04x faster                                                      |
| xml_etree_iterparse      | 62.3 ms                                                         | 60.7 ms: 1.03x faster                                                     |
| regex_dna                | 119 ms                                                          | 116 ms: 1.03x faster                                                      |
| pidigits                 | 150 ms                                                          | 146 ms: 1.02x faster                                                      |
| regex_effbot             | 1.58 ms                                                         | 1.55 ms: 1.02x faster                                                     |
| pprint_safe_repr         | 474 ms                                                          | 466 ms: 1.02x faster                                                      |
| pprint_pformat           | 966 ms                                                          | 951 ms: 1.02x faster                                                      |
| sqlite_synth             | 1.60 us                                                         | 1.57 us: 1.02x faster                                                     |
| pickle_pure_python       | 175 us                                                          | 173 us: 1.01x faster                                                      |
| json_loads               | 14.2 us                                                         | 14.0 us: 1.01x faster                                                     |
| json_dumps               | 5.61 ms                                                         | 5.55 ms: 1.01x faster                                                     |
| gc_traversal             | 1.55 ms                                                         | 1.54 ms: 1.01x faster                                                     |
| xml_etree_parse          | 90.9 ms                                                         | 90.1 ms: 1.01x faster                                                     |
| deepcopy_reduce          | 1.99 us                                                         | 1.98 us: 1.01x faster                                                     |
| logging_silent           | 52.9 ns                                                         | 53.1 ns: 1.00x slower                                                     |
| telco                    | 4.67 ms                                                         | 4.69 ms: 1.01x slower                                                     |
| logging_format           | 6.22 us                                                         | 6.27 us: 1.01x slower                                                     |
| unpickle                 | 8.40 us                                                         | 8.50 us: 1.01x slower                                                     |
| logging_simple           | 5.78 us                                                         | 5.86 us: 1.01x slower                                                     |
| xml_etree_process        | 36.4 ms                                                         | 37.1 ms: 1.02x slower                                                     |
| pickle_dict              | 18.1 us                                                         | 18.5 us: 1.02x slower                                                     |
| pickle                   | 7.11 us                                                         | 7.26 us: 1.02x slower                                                     |
| pathlib                  | 75.9 ms                                                         | 77.4 ms: 1.02x slower                                                     |
| deepcopy                 | 220 us                                                          | 225 us: 1.02x slower                                                      |
| aiohttp                  | 889 us                                                          | 909 us: 1.02x slower                                                      |
| async_tree_io_tg         | 605 ms                                                          | 619 ms: 1.02x slower                                                      |
| generators               | 19.6 ms                                                         | 20.0 ms: 1.02x slower                                                     |
| unpickle_pure_python     | 122 us                                                          | 125 us: 1.03x slower                                                      |
| meteor_contest           | 69.9 ms                                                         | 72.0 ms: 1.03x slower                                                     |
| coroutines               | 12.8 ms                                                         | 13.2 ms: 1.04x slower                                                     |
| comprehensions           | 10.4 us                                                         | 10.8 us: 1.04x slower                                                     |
| sympy_sum                | 84.4 ms                                                         | 87.7 ms: 1.04x slower                                                     |
| docutils                 | 1.63 sec                                                        | 1.69 sec: 1.04x slower                                                    |
| bench_mp_pool            | 64.8 ms                                                         | 67.4 ms: 1.04x slower                                                     |
| sqlglot_parse            | 748 us                                                          | 779 us: 1.04x slower                                                      |
| sqlglot_transpile        | 955 us                                                          | 995 us: 1.04x slower                                                      |
| html5lib                 | 35.0 ms                                                         | 36.5 ms: 1.04x slower                                                     |
| tornado_http             | 81.8 ms                                                         | 85.5 ms: 1.04x slower                                                     |
| genshi_text              | 14.4 ms                                                         | 15.1 ms: 1.05x slower                                                     |
| sympy_str                | 159 ms                                                          | 167 ms: 1.05x slower                                                      |
| scimark_sor              | 75.3 ms                                                         | 79.3 ms: 1.05x slower                                                     |
| 2to3                     | 207 ms                                                          | 218 ms: 1.05x slower                                                      |
| unpickle_list            | 2.62 us                                                         | 2.77 us: 1.06x slower                                                     |
| sympy_expand             | 271 ms                                                          | 288 ms: 1.06x slower                                                      |
| nqueens                  | 56.7 ms                                                         | 60.4 ms: 1.07x slower                                                     |
| sqlglot_normalize        | 173 ms                                                          | 186 ms: 1.07x slower                                                      |
| regex_compile            | 78.0 ms                                                         | 83.8 ms: 1.07x slower                                                     |
| django_template          | 21.7 ms                                                         | 23.3 ms: 1.08x slower                                                     |
| genshi_xml               | 31.6 ms                                                         | 34.0 ms: 1.08x slower                                                     |
| sympy_integrate          | 12.2 ms                                                         | 13.2 ms: 1.08x slower                                                     |
| python_startup           | 20.3 ms                                                         | 22.0 ms: 1.08x slower                                                     |
| mypy2                    | 418 ms                                                          | 453 ms: 1.08x slower                                                      |
| bench_thread_pool        | 768 us                                                          | 833 us: 1.08x slower                                                      |
| raytrace                 | 162 ms                                                          | 176 ms: 1.09x slower                                                      |
| richards_super           | 30.2 ms                                                         | 32.7 ms: 1.09x slower                                                     |
| dulwich_log              | 38.0 ms                                                         | 41.5 ms: 1.09x slower                                                     |
| deltablue                | 1.88 ms                                                         | 2.06 ms: 1.09x slower                                                     |
| sqlglot_optimize         | 32.7 ms                                                         | 35.8 ms: 1.09x slower                                                     |
| richards                 | 26.7 ms                                                         | 29.5 ms: 1.10x slower                                                     |
| async_generators         | 223 ms                                                          | 247 ms: 1.10x slower                                                      |
| coverage                 | 42.1 ms                                                         | 46.7 ms: 1.11x slower                                                     |
| thrift                   | 8.11 ms                                                         | 9.19 ms: 1.13x slower                                                     |
| mdp                      | 1.31 sec                                                        | 1.51 sec: 1.15x slower                                                    |
| go                       | 82.1 ms                                                         | 95.3 ms: 1.16x slower                                                     |
| hexiom                   | 3.72 ms                                                         | 4.47 ms: 1.20x slower                                                     |
| python_startup_no_site   | 16.2 ms                                                         | 19.6 ms: 1.21x slower                                                     |
| scimark_lu               | 56.6 ms                                                         | 71.8 ms: 1.27x slower                                                     |
| Geometric mean           | (ref)                                                           | 1.01x slower                                                              |

Benchmark hidden because not significant (13): pycparser, async_tree_none, pickle_list, chaos, chameleon, xml_etree_generate, async_tree_cpu_io_mixed_tg, deepcopy_memo, async_tree_none_tg, asyncio_tcp, async_tree_memoization, asyncio_tcp_ssl, async_tree_memoization_tg
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17.json: flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-pythonperf1-amd64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: unpack_sequence

# HPT report

- Reliability score: 97.98% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown