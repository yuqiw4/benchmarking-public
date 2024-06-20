# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 168 ms: 1.05x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.47 ms: 1.05x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.49 sec: 1.04x slower                                                 |
| tornado_http   | 66.7 ms                                                    | 76.6 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                      | 1.05x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none                  | 209 ms                                                     | 201 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 363 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 465 ms: 1.03x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 42.9 ms: 1.04x slower                                                  |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 130 ms: 1.04x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 64.0 ms: 1.06x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 259 ms: 1.08x slower                                                   |
| Geometric mean                   | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (8): async_tree_eager_io_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io, async_tree_eager_io, async_tree_eager_memoization, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 282 ms: 1.00x slower                                                   |
| nbody          | 59.6 ms                                                    | 70.1 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                      | 1.06x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.58 ms                                                    | 2.57 ms: 1.00x faster                                                  |
| regex_v8       | 17.3 ms                                                    | 17.4 ms: 1.01x slower                                                  |
| regex_compile  | 68.5 ms                                                    | 83.3 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                      | 1.05x slower                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 1.47 sec                                                   | 1.26 sec: 1.16x faster                                                 |
| xml_etree_parse      | 106 ms                                                     | 97.8 ms: 1.08x faster                                                  |
| xml_etree_iterparse  | 71.5 ms                                                    | 67.7 ms: 1.06x faster                                                  |
| unpickle_pure_python | 141 us                                                     | 135 us: 1.04x faster                                                   |
| xml_etree_process    | 37.1 ms                                                    | 36.7 ms: 1.01x faster                                                  |
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| pickle               | 7.48 us                                                    | 7.43 us: 1.01x faster                                                  |
| xml_etree_generate   | 52.7 ms                                                    | 52.8 ms: 1.00x slower                                                  |
| pickle_pure_python   | 179 us                                                     | 180 us: 1.01x slower                                                   |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| unpickle_list        | 2.88 us                                                    | 2.93 us: 1.02x slower                                                  |
| pickle_list          | 2.96 us                                                    | 3.01 us: 1.02x slower                                                  |
| json_dumps           | 6.23 ms                                                    | 6.35 ms: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                      | 1.02x faster                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 12.3 ms                                                    | 10.5 ms: 1.17x faster                                                  |
| python_startup         | 15.2 ms                                                    | 13.3 ms: 1.14x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.16x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 6.87 ms: 1.02x faster                                                  |
| genshi_xml      | 29.9 ms                                                    | 30.8 ms: 1.03x slower                                                  |
| genshi_text     | 13.9 ms                                                    | 14.6 ms: 1.05x slower                                                  |
| django_template | 19.4 ms                                                    | 20.4 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols         | 87.6 us                                                    | 68.1 us: 1.29x faster                                                  |
| python_startup_no_site           | 12.3 ms                                                    | 10.5 ms: 1.17x faster                                                  |
| tomli_loads                      | 1.47 sec                                                   | 1.26 sec: 1.16x faster                                                 |
| python_startup                   | 15.2 ms                                                    | 13.3 ms: 1.14x faster                                                  |
| xml_etree_parse                  | 106 ms                                                     | 97.8 ms: 1.08x faster                                                  |
| richards                         | 31.8 ms                                                    | 29.5 ms: 1.08x faster                                                  |
| richards_super                   | 35.2 ms                                                    | 32.8 ms: 1.07x faster                                                  |
| crypto_pyaes                     | 49.5 ms                                                    | 46.2 ms: 1.07x faster                                                  |
| xml_etree_iterparse              | 71.5 ms                                                    | 67.7 ms: 1.06x faster                                                  |
| async_tree_none                  | 209 ms                                                     | 201 ms: 1.04x faster                                                   |
| unpickle_pure_python             | 141 us                                                     | 135 us: 1.04x faster                                                   |
| create_gc_cycles                 | 897 us                                                     | 872 us: 1.03x faster                                                   |
| bench_mp_pool                    | 47.2 ms                                                    | 46.2 ms: 1.02x faster                                                  |
| pyflate                          | 321 ms                                                     | 314 ms: 1.02x faster                                                   |
| mako                             | 6.99 ms                                                    | 6.87 ms: 1.02x faster                                                  |
| xml_etree_process                | 37.1 ms                                                    | 36.7 ms: 1.01x faster                                                  |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| pickle                           | 7.48 us                                                    | 7.43 us: 1.01x faster                                                  |
| json                             | 2.93 ms                                                    | 2.91 ms: 1.01x faster                                                  |
| telco                            | 4.60 ms                                                    | 4.58 ms: 1.00x faster                                                  |
| regex_effbot                     | 2.58 ms                                                    | 2.57 ms: 1.00x faster                                                  |
| pidigits                         | 282 ms                                                     | 282 ms: 1.00x slower                                                   |
| xml_etree_generate               | 52.7 ms                                                    | 52.8 ms: 1.00x slower                                                  |
| thrift                           | 435 us                                                     | 437 us: 1.00x slower                                                   |
| pickle_pure_python               | 179 us                                                     | 180 us: 1.01x slower                                                   |
| regex_v8                         | 17.3 ms                                                    | 17.4 ms: 1.01x slower                                                  |
| pathlib                          | 23.3 ms                                                    | 23.5 ms: 1.01x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                   |
| logging_simple                   | 3.04 us                                                    | 3.07 us: 1.01x slower                                                  |
| logging_format                   | 3.31 us                                                    | 3.34 us: 1.01x slower                                                  |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| deepcopy_reduce                  | 1.82 us                                                    | 1.84 us: 1.01x slower                                                  |
| scimark_monte_carlo              | 42.5 ms                                                    | 43.0 ms: 1.01x slower                                                  |
| sqlite_synth                     | 1.55 us                                                    | 1.57 us: 1.01x slower                                                  |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 363 ms: 1.02x slower                                                   |
| unpickle_list                    | 2.88 us                                                    | 2.93 us: 1.02x slower                                                  |
| pickle_list                      | 2.96 us                                                    | 3.01 us: 1.02x slower                                                  |
| json_dumps                       | 6.23 ms                                                    | 6.35 ms: 1.02x slower                                                  |
| pycparser                        | 632 ms                                                     | 645 ms: 1.02x slower                                                   |
| mdp                              | 1.53 sec                                                   | 1.57 sec: 1.02x slower                                                 |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.32 sec: 1.02x slower                                                 |
| genshi_xml                       | 29.9 ms                                                    | 30.8 ms: 1.03x slower                                                  |
| dulwich_log                      | 27.6 ms                                                    | 28.4 ms: 1.03x slower                                                  |
| coverage                         | 45.0 ms                                                    | 46.4 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 465 ms: 1.03x slower                                                   |
| sqlglot_parse                    | 732 us                                                     | 758 us: 1.04x slower                                                   |
| sympy_expand                     | 226 ms                                                     | 234 ms: 1.04x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 42.9 ms: 1.04x slower                                                  |
| deepcopy                         | 204 us                                                     | 212 us: 1.04x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 130 ms: 1.04x slower                                                   |
| fannkuch                         | 248 ms                                                     | 258 ms: 1.04x slower                                                   |
| meteor_contest                   | 70.3 ms                                                    | 73.1 ms: 1.04x slower                                                  |
| docutils                         | 1.44 sec                                                   | 1.49 sec: 1.04x slower                                                 |
| sqlglot_transpile                | 891 us                                                     | 929 us: 1.04x slower                                                   |
| sqlglot_normalize                | 166 ms                                                     | 173 ms: 1.04x slower                                                   |
| 2to3                             | 161 ms                                                     | 168 ms: 1.05x slower                                                   |
| pprint_safe_repr                 | 465 ms                                                     | 486 ms: 1.05x slower                                                   |
| chameleon                        | 4.27 ms                                                    | 4.47 ms: 1.05x slower                                                  |
| genshi_text                      | 13.9 ms                                                    | 14.6 ms: 1.05x slower                                                  |
| pprint_pformat                   | 947 ms                                                     | 995 ms: 1.05x slower                                                   |
| async_generators                 | 281 ms                                                     | 296 ms: 1.05x slower                                                   |
| django_template                  | 19.4 ms                                                    | 20.4 ms: 1.05x slower                                                  |
| go                               | 101 ms                                                     | 106 ms: 1.06x slower                                                   |
| logging_silent                   | 60.1 ns                                                    | 63.5 ns: 1.06x slower                                                  |
| sympy_str                        | 131 ms                                                     | 139 ms: 1.06x slower                                                   |
| mypy2                            | 379 ms                                                     | 402 ms: 1.06x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 64.0 ms: 1.06x slower                                                  |
| deepcopy_memo                    | 22.6 us                                                    | 24.1 us: 1.07x slower                                                  |
| sqlglot_optimize                 | 30.9 ms                                                    | 33.1 ms: 1.07x slower                                                  |
| sympy_integrate                  | 10.3 ms                                                    | 11.2 ms: 1.08x slower                                                  |
| sympy_sum                        | 69.2 ms                                                    | 74.8 ms: 1.08x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 259 ms: 1.08x slower                                                   |
| coroutines                       | 15.8 ms                                                    | 17.2 ms: 1.09x slower                                                  |
| bench_thread_pool                | 447 us                                                     | 487 us: 1.09x slower                                                   |
| raytrace                         | 147 ms                                                     | 163 ms: 1.11x slower                                                   |
| scimark_sor                      | 94.9 ms                                                    | 105 ms: 1.11x slower                                                   |
| scimark_fft                      | 181 ms                                                     | 201 ms: 1.11x slower                                                   |
| spectral_norm                    | 66.4 ms                                                    | 73.7 ms: 1.11x slower                                                  |
| chaos                            | 34.0 ms                                                    | 37.9 ms: 1.11x slower                                                  |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.12 ms: 1.12x slower                                                  |
| aiohttp                          | 997 us                                                     | 1.12 ms: 1.13x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 59.3 ms: 1.14x slower                                                  |
| gunicorn                         | 1.04 ms                                                    | 1.19 ms: 1.15x slower                                                  |
| tornado_http                     | 66.7 ms                                                    | 76.6 ms: 1.15x slower                                                  |
| generators                       | 22.9 ms                                                    | 26.4 ms: 1.15x slower                                                  |
| deltablue                        | 2.14 ms                                                    | 2.47 ms: 1.15x slower                                                  |
| hexiom                           | 4.06 ms                                                    | 4.71 ms: 1.16x slower                                                  |
| comprehensions                   | 10.2 us                                                    | 11.8 us: 1.16x slower                                                  |
| nbody                            | 59.6 ms                                                    | 70.1 ms: 1.18x slower                                                  |
| regex_compile                    | 68.5 ms                                                    | 83.3 ms: 1.22x slower                                                  |
| scimark_lu                       | 66.9 ms                                                    | 81.6 ms: 1.22x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.03x slower                                                           |

Benchmark hidden because not significant (17): async_tree_eager_io_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io, dask, html5lib, asyncio_websockets, regex_dna, gc_traversal, float, unpickle, async_tree_eager_io, async_tree_eager_memoization, asyncio_tcp, async_tree_memoization, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.17x