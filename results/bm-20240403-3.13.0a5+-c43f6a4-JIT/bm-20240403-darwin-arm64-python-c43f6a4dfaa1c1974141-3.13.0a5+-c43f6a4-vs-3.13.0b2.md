# Results vs. 3.13.0b2

- fork: python
- ref: c43f6a4dfaa1c1974141
- machine: darwin-arm64
- commit hash: c43f6a4
- commit date: 2024-04-03
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 173 ms: 1.07x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.48 ms: 1.05x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.56 sec: 1.08x slower                                                 |
| html5lib       | 31.2 ms                                                    | 33.3 ms: 1.07x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 76.9 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                      | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none                  | 209 ms                                                     | 204 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 365 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 467 ms: 1.04x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.0 ms: 1.04x slower                                                  |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.05x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 64.9 ms: 1.08x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 261 ms: 1.09x slower                                                   |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                           |

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, async_tree_eager_io_tg, async_tree_io_tg, async_tree_none_tg, async_tree_io, async_tree_memoization, async_tree_eager_io, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 48.6 ms                                                    | 49.1 ms: 1.01x slower                                                  |
| nbody          | 59.6 ms                                                    | 70.5 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                      | 1.06x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 17.2 ms: 1.01x faster                                                  |
| regex_effbot   | 2.58 ms                                                    | 2.61 ms: 1.01x slower                                                  |
| regex_dna      | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| regex_compile  | 68.5 ms                                                    | 80.5 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                      | 1.05x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|---------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads         | 1.47 sec                                                   | 1.29 sec: 1.14x faster                                                 |
| pickle_dict         | 18.3 us                                                    | 18.0 us: 1.01x faster                                                  |
| json_loads          | 16.8 us                                                    | 16.9 us: 1.00x slower                                                  |
| pickle_list         | 2.96 us                                                    | 2.97 us: 1.01x slower                                                  |
| pickle              | 7.48 us                                                    | 7.52 us: 1.01x slower                                                  |
| xml_etree_iterparse | 71.5 ms                                                    | 72.3 ms: 1.01x slower                                                  |
| unpickle            | 9.12 us                                                    | 9.30 us: 1.02x slower                                                  |
| pickle_pure_python  | 179 us                                                     | 183 us: 1.02x slower                                                   |
| json_dumps          | 6.23 ms                                                    | 6.39 ms: 1.03x slower                                                  |
| xml_etree_generate  | 52.7 ms                                                    | 54.2 ms: 1.03x slower                                                  |
| unpickle_list       | 2.88 us                                                    | 3.02 us: 1.05x slower                                                  |
| Geometric mean      | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (3): unpickle_pure_python, xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 13.4 ms: 1.14x faster                                                  |
| python_startup_no_site | 12.3 ms                                                    | 11.6 ms: 1.06x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.10x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 6.99 ms                                                    | 6.96 ms: 1.00x faster                                                  |
| genshi_text    | 13.9 ms                                                    | 14.7 ms: 1.06x slower                                                  |
| genshi_xml     | 29.9 ms                                                    | 31.7 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                      | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240403-darwin-arm64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols         | 87.6 us                                                    | 69.3 us: 1.26x faster                                                  |
| tomli_loads                      | 1.47 sec                                                   | 1.29 sec: 1.14x faster                                                 |
| python_startup                   | 15.2 ms                                                    | 13.4 ms: 1.14x faster                                                  |
| pylint                           | 170 ms                                                     | 155 ms: 1.10x faster                                                   |
| crypto_pyaes                     | 49.5 ms                                                    | 46.6 ms: 1.06x faster                                                  |
| python_startup_no_site           | 12.3 ms                                                    | 11.6 ms: 1.06x faster                                                  |
| async_tree_none                  | 209 ms                                                     | 204 ms: 1.03x faster                                                   |
| telco                            | 4.60 ms                                                    | 4.51 ms: 1.02x faster                                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 46.3 ms: 1.02x faster                                                  |
| pickle_dict                      | 18.3 us                                                    | 18.0 us: 1.01x faster                                                  |
| regex_v8                         | 17.3 ms                                                    | 17.2 ms: 1.01x faster                                                  |
| mako                             | 6.99 ms                                                    | 6.96 ms: 1.00x faster                                                  |
| richards                         | 31.8 ms                                                    | 31.7 ms: 1.00x faster                                                  |
| richards_super                   | 35.2 ms                                                    | 35.1 ms: 1.00x faster                                                  |
| asyncio_websockets               | 409 ms                                                     | 410 ms: 1.00x slower                                                   |
| json_loads                       | 16.8 us                                                    | 16.9 us: 1.00x slower                                                  |
| gc_traversal                     | 2.45 ms                                                    | 2.46 ms: 1.00x slower                                                  |
| pickle_list                      | 2.96 us                                                    | 2.97 us: 1.01x slower                                                  |
| pickle                           | 7.48 us                                                    | 7.52 us: 1.01x slower                                                  |
| json                             | 2.93 ms                                                    | 2.96 ms: 1.01x slower                                                  |
| pyflate                          | 321 ms                                                     | 324 ms: 1.01x slower                                                   |
| thrift                           | 435 us                                                     | 439 us: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 334 ms: 1.01x slower                                                   |
| float                            | 48.6 ms                                                    | 49.1 ms: 1.01x slower                                                  |
| xml_etree_iterparse              | 71.5 ms                                                    | 72.3 ms: 1.01x slower                                                  |
| regex_effbot                     | 2.58 ms                                                    | 2.61 ms: 1.01x slower                                                  |
| scimark_monte_carlo              | 42.5 ms                                                    | 43.2 ms: 1.02x slower                                                  |
| regex_dna                        | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| unpickle                         | 9.12 us                                                    | 9.30 us: 1.02x slower                                                  |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 365 ms: 1.02x slower                                                   |
| coverage                         | 45.0 ms                                                    | 45.9 ms: 1.02x slower                                                  |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.32 sec: 1.02x slower                                                 |
| pickle_pure_python               | 179 us                                                     | 183 us: 1.02x slower                                                   |
| mdp                              | 1.53 sec                                                   | 1.57 sec: 1.03x slower                                                 |
| json_dumps                       | 6.23 ms                                                    | 6.39 ms: 1.03x slower                                                  |
| logging_simple                   | 3.04 us                                                    | 3.13 us: 1.03x slower                                                  |
| sqlite_synth                     | 1.55 us                                                    | 1.60 us: 1.03x slower                                                  |
| logging_format                   | 3.31 us                                                    | 3.41 us: 1.03x slower                                                  |
| xml_etree_generate               | 52.7 ms                                                    | 54.2 ms: 1.03x slower                                                  |
| deepcopy_reduce                  | 1.82 us                                                    | 1.88 us: 1.03x slower                                                  |
| pycparser                        | 632 ms                                                     | 651 ms: 1.03x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 467 ms: 1.04x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.0 ms: 1.04x slower                                                  |
| fannkuch                         | 248 ms                                                     | 259 ms: 1.04x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.05x slower                                                   |
| meteor_contest                   | 70.3 ms                                                    | 73.5 ms: 1.05x slower                                                  |
| deepcopy                         | 204 us                                                     | 214 us: 1.05x slower                                                   |
| unpickle_list                    | 2.88 us                                                    | 3.02 us: 1.05x slower                                                  |
| chameleon                        | 4.27 ms                                                    | 4.48 ms: 1.05x slower                                                  |
| sympy_expand                     | 226 ms                                                     | 238 ms: 1.05x slower                                                   |
| sqlglot_transpile                | 891 us                                                     | 940 us: 1.06x slower                                                   |
| genshi_text                      | 13.9 ms                                                    | 14.7 ms: 1.06x slower                                                  |
| dulwich_log                      | 27.6 ms                                                    | 29.1 ms: 1.06x slower                                                  |
| sqlglot_parse                    | 732 us                                                     | 774 us: 1.06x slower                                                   |
| go                               | 101 ms                                                     | 106 ms: 1.06x slower                                                   |
| genshi_xml                       | 29.9 ms                                                    | 31.7 ms: 1.06x slower                                                  |
| logging_silent                   | 60.1 ns                                                    | 63.8 ns: 1.06x slower                                                  |
| coroutines                       | 15.8 ms                                                    | 16.8 ms: 1.06x slower                                                  |
| deltablue                        | 2.14 ms                                                    | 2.27 ms: 1.06x slower                                                  |
| pprint_safe_repr                 | 465 ms                                                     | 493 ms: 1.06x slower                                                   |
| sqlglot_normalize                | 166 ms                                                     | 176 ms: 1.06x slower                                                   |
| pathlib                          | 23.3 ms                                                    | 24.9 ms: 1.07x slower                                                  |
| pprint_pformat                   | 947 ms                                                     | 1.01 sec: 1.07x slower                                                 |
| html5lib                         | 31.2 ms                                                    | 33.3 ms: 1.07x slower                                                  |
| 2to3                             | 161 ms                                                     | 173 ms: 1.07x slower                                                   |
| aiohttp                          | 997 us                                                     | 1.07 ms: 1.08x slower                                                  |
| async_tree_eager                 | 60.3 ms                                                    | 64.9 ms: 1.08x slower                                                  |
| async_generators                 | 281 ms                                                     | 302 ms: 1.08x slower                                                   |
| sympy_str                        | 131 ms                                                     | 142 ms: 1.08x slower                                                   |
| deepcopy_memo                    | 22.6 us                                                    | 24.4 us: 1.08x slower                                                  |
| docutils                         | 1.44 sec                                                   | 1.56 sec: 1.08x slower                                                 |
| mypy2                            | 379 ms                                                     | 412 ms: 1.09x slower                                                   |
| async_tree_memoization_tg        | 240 ms                                                     | 261 ms: 1.09x slower                                                   |
| sqlglot_optimize                 | 30.9 ms                                                    | 33.7 ms: 1.09x slower                                                  |
| bench_thread_pool                | 447 us                                                     | 490 us: 1.10x slower                                                   |
| sympy_integrate                  | 10.3 ms                                                    | 11.4 ms: 1.10x slower                                                  |
| scimark_fft                      | 181 ms                                                     | 200 ms: 1.11x slower                                                   |
| sympy_sum                        | 69.2 ms                                                    | 76.8 ms: 1.11x slower                                                  |
| spectral_norm                    | 66.4 ms                                                    | 73.7 ms: 1.11x slower                                                  |
| scimark_sor                      | 94.9 ms                                                    | 106 ms: 1.12x slower                                                   |
| chaos                            | 34.0 ms                                                    | 38.3 ms: 1.13x slower                                                  |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.13 ms: 1.13x slower                                                  |
| gunicorn                         | 1.04 ms                                                    | 1.17 ms: 1.13x slower                                                  |
| generators                       | 22.9 ms                                                    | 26.1 ms: 1.14x slower                                                  |
| tornado_http                     | 66.7 ms                                                    | 76.9 ms: 1.15x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 60.5 ms: 1.16x slower                                                  |
| raytrace                         | 147 ms                                                     | 172 ms: 1.17x slower                                                   |
| regex_compile                    | 68.5 ms                                                    | 80.5 ms: 1.17x slower                                                  |
| comprehensions                   | 10.2 us                                                    | 12.0 us: 1.18x slower                                                  |
| nbody                            | 59.6 ms                                                    | 70.5 ms: 1.18x slower                                                  |
| hexiom                           | 4.06 ms                                                    | 4.82 ms: 1.19x slower                                                  |
| scimark_lu                       | 66.9 ms                                                    | 81.7 ms: 1.22x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.04x slower                                                           |

Benchmark hidden because not significant (15): async_tree_cpu_io_mixed, async_tree_eager_io_tg, async_tree_io_tg, unpickle_pure_python, xml_etree_process, async_tree_none_tg, create_gc_cycles, pidigits, dask, async_tree_io, async_tree_memoization, xml_etree_parse, async_tree_eager_io, async_tree_eager_memoization, asyncio_tcp
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.18x