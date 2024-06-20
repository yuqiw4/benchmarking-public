# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| chameleon      | 4.27 ms                                                    | 4.49 ms: 1.05x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.45 sec: 1.01x slower                                                 |
| html5lib       | 31.2 ms                                                    | 31.9 ms: 1.02x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 75.0 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                      | 1.04x slower                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none                  | 209 ms                                                     | 202 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 365 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 466 ms: 1.03x slower                                                   |
| async_tree_memoization           | 260 ms                                                     | 270 ms: 1.04x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.04x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 63.0 ms: 1.04x slower                                                  |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.4 ms: 1.05x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 259 ms: 1.08x slower                                                   |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                           |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_io, async_tree_eager_memoization, async_tree_eager_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 48.6 ms                                                    | 50.8 ms: 1.05x slower                                                  |
| nbody          | 59.6 ms                                                    | 65.2 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                      | 1.05x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 17.4 ms: 1.01x slower                                                  |
| regex_compile  | 68.5 ms                                                    | 69.4 ms: 1.01x slower                                                  |
| regex_effbot   | 2.58 ms                                                    | 2.63 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 106 ms                                                     | 99.0 ms: 1.07x faster                                                  |
| xml_etree_iterparse  | 71.5 ms                                                    | 68.8 ms: 1.04x faster                                                  |
| pickle               | 7.48 us                                                    | 7.44 us: 1.01x faster                                                  |
| pickle_dict          | 18.3 us                                                    | 18.2 us: 1.01x faster                                                  |
| json_dumps           | 6.23 ms                                                    | 6.26 ms: 1.01x slower                                                  |
| unpickle_list        | 2.88 us                                                    | 2.90 us: 1.01x slower                                                  |
| json_loads           | 16.8 us                                                    | 17.1 us: 1.01x slower                                                  |
| unpickle_pure_python | 141 us                                                     | 143 us: 1.02x slower                                                   |
| pickle_list          | 2.96 us                                                    | 3.01 us: 1.02x slower                                                  |
| xml_etree_process    | 37.1 ms                                                    | 37.9 ms: 1.02x slower                                                  |
| tomli_loads          | 1.47 sec                                                   | 1.50 sec: 1.02x slower                                                 |
| pickle_pure_python   | 179 us                                                     | 183 us: 1.02x slower                                                   |
| xml_etree_generate   | 52.7 ms                                                    | 54.9 ms: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                      | 1.00x slower                                                           |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 12.3 ms                                                    | 9.12 ms: 1.35x faster                                                  |
| python_startup         | 15.2 ms                                                    | 11.9 ms: 1.28x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.31x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 7.14 ms: 1.02x slower                                                  |
| django_template | 19.4 ms                                                    | 20.1 ms: 1.03x slower                                                  |
| genshi_text     | 13.9 ms                                                    | 14.7 ms: 1.05x slower                                                  |
| genshi_xml      | 29.9 ms                                                    | 31.7 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site           | 12.3 ms                                                    | 9.12 ms: 1.35x faster                                                  |
| typing_runtime_protocols         | 87.6 us                                                    | 68.0 us: 1.29x faster                                                  |
| python_startup                   | 15.2 ms                                                    | 11.9 ms: 1.28x faster                                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 43.1 ms: 1.09x faster                                                  |
| xml_etree_parse                  | 106 ms                                                     | 99.0 ms: 1.07x faster                                                  |
| crypto_pyaes                     | 49.5 ms                                                    | 46.5 ms: 1.06x faster                                                  |
| xml_etree_iterparse              | 71.5 ms                                                    | 68.8 ms: 1.04x faster                                                  |
| async_tree_none                  | 209 ms                                                     | 202 ms: 1.03x faster                                                   |
| create_gc_cycles                 | 897 us                                                     | 872 us: 1.03x faster                                                   |
| richards_super                   | 35.2 ms                                                    | 34.3 ms: 1.03x faster                                                  |
| richards                         | 31.8 ms                                                    | 31.2 ms: 1.02x faster                                                  |
| pickle                           | 7.48 us                                                    | 7.44 us: 1.01x faster                                                  |
| pickle_dict                      | 18.3 us                                                    | 18.2 us: 1.01x faster                                                  |
| gc_traversal                     | 2.45 ms                                                    | 2.44 ms: 1.00x faster                                                  |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                   |
| sqlite_synth                     | 1.55 us                                                    | 1.56 us: 1.00x slower                                                  |
| json_dumps                       | 6.23 ms                                                    | 6.26 ms: 1.01x slower                                                  |
| pyflate                          | 321 ms                                                     | 322 ms: 1.01x slower                                                   |
| unpickle_list                    | 2.88 us                                                    | 2.90 us: 1.01x slower                                                  |
| regex_v8                         | 17.3 ms                                                    | 17.4 ms: 1.01x slower                                                  |
| sympy_integrate                  | 10.3 ms                                                    | 10.4 ms: 1.01x slower                                                  |
| json                             | 2.93 ms                                                    | 2.96 ms: 1.01x slower                                                  |
| telco                            | 4.60 ms                                                    | 4.65 ms: 1.01x slower                                                  |
| docutils                         | 1.44 sec                                                   | 1.45 sec: 1.01x slower                                                 |
| pycparser                        | 632 ms                                                     | 640 ms: 1.01x slower                                                   |
| regex_compile                    | 68.5 ms                                                    | 69.4 ms: 1.01x slower                                                  |
| json_loads                       | 16.8 us                                                    | 17.1 us: 1.01x slower                                                  |
| unpickle_pure_python             | 141 us                                                     | 143 us: 1.02x slower                                                   |
| sympy_expand                     | 226 ms                                                     | 229 ms: 1.02x slower                                                   |
| sympy_str                        | 131 ms                                                     | 134 ms: 1.02x slower                                                   |
| deltablue                        | 2.14 ms                                                    | 2.18 ms: 1.02x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.02x slower                                                   |
| pickle_list                      | 2.96 us                                                    | 3.01 us: 1.02x slower                                                  |
| async_generators                 | 281 ms                                                     | 286 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 365 ms: 1.02x slower                                                   |
| regex_effbot                     | 2.58 ms                                                    | 2.63 ms: 1.02x slower                                                  |
| sqlglot_transpile                | 891 us                                                     | 908 us: 1.02x slower                                                   |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.32 sec: 1.02x slower                                                 |
| sympy_sum                        | 69.2 ms                                                    | 70.6 ms: 1.02x slower                                                  |
| sqlglot_optimize                 | 30.9 ms                                                    | 31.5 ms: 1.02x slower                                                  |
| thrift                           | 435 us                                                     | 444 us: 1.02x slower                                                   |
| meteor_contest                   | 70.3 ms                                                    | 71.8 ms: 1.02x slower                                                  |
| sqlglot_normalize                | 166 ms                                                     | 169 ms: 1.02x slower                                                   |
| mako                             | 6.99 ms                                                    | 7.14 ms: 1.02x slower                                                  |
| xml_etree_process                | 37.1 ms                                                    | 37.9 ms: 1.02x slower                                                  |
| sqlglot_parse                    | 732 us                                                     | 749 us: 1.02x slower                                                   |
| tomli_loads                      | 1.47 sec                                                   | 1.50 sec: 1.02x slower                                                 |
| html5lib                         | 31.2 ms                                                    | 31.9 ms: 1.02x slower                                                  |
| pickle_pure_python               | 179 us                                                     | 183 us: 1.02x slower                                                   |
| pprint_pformat                   | 947 ms                                                     | 972 ms: 1.03x slower                                                   |
| pathlib                          | 23.3 ms                                                    | 24.0 ms: 1.03x slower                                                  |
| scimark_lu                       | 66.9 ms                                                    | 68.9 ms: 1.03x slower                                                  |
| pprint_safe_repr                 | 465 ms                                                     | 479 ms: 1.03x slower                                                   |
| logging_format                   | 3.31 us                                                    | 3.42 us: 1.03x slower                                                  |
| django_template                  | 19.4 ms                                                    | 20.1 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 466 ms: 1.03x slower                                                   |
| logging_simple                   | 3.04 us                                                    | 3.15 us: 1.04x slower                                                  |
| fannkuch                         | 248 ms                                                     | 258 ms: 1.04x slower                                                   |
| raytrace                         | 147 ms                                                     | 153 ms: 1.04x slower                                                   |
| comprehensions                   | 10.2 us                                                    | 10.6 us: 1.04x slower                                                  |
| async_tree_memoization           | 260 ms                                                     | 270 ms: 1.04x slower                                                   |
| xml_etree_generate               | 52.7 ms                                                    | 54.9 ms: 1.04x slower                                                  |
| deepcopy_reduce                  | 1.82 us                                                    | 1.90 us: 1.04x slower                                                  |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.04x slower                                                   |
| hexiom                           | 4.06 ms                                                    | 4.24 ms: 1.04x slower                                                  |
| async_tree_eager                 | 60.3 ms                                                    | 63.0 ms: 1.04x slower                                                  |
| float                            | 48.6 ms                                                    | 50.8 ms: 1.05x slower                                                  |
| coverage                         | 45.0 ms                                                    | 47.1 ms: 1.05x slower                                                  |
| scimark_sor                      | 94.9 ms                                                    | 99.4 ms: 1.05x slower                                                  |
| scimark_monte_carlo              | 42.5 ms                                                    | 44.5 ms: 1.05x slower                                                  |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.4 ms: 1.05x slower                                                  |
| chameleon                        | 4.27 ms                                                    | 4.49 ms: 1.05x slower                                                  |
| genshi_text                      | 13.9 ms                                                    | 14.7 ms: 1.05x slower                                                  |
| deepcopy                         | 204 us                                                     | 216 us: 1.06x slower                                                   |
| bench_thread_pool                | 447 us                                                     | 472 us: 1.06x slower                                                   |
| deepcopy_memo                    | 22.6 us                                                    | 23.9 us: 1.06x slower                                                  |
| gunicorn                         | 1.04 ms                                                    | 1.10 ms: 1.06x slower                                                  |
| genshi_xml                       | 29.9 ms                                                    | 31.7 ms: 1.06x slower                                                  |
| chaos                            | 34.0 ms                                                    | 36.3 ms: 1.07x slower                                                  |
| spectral_norm                    | 66.4 ms                                                    | 71.0 ms: 1.07x slower                                                  |
| aiohttp                          | 997 us                                                     | 1.07 ms: 1.08x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 56.3 ms: 1.08x slower                                                  |
| logging_silent                   | 60.1 ns                                                    | 64.8 ns: 1.08x slower                                                  |
| scimark_fft                      | 181 ms                                                     | 195 ms: 1.08x slower                                                   |
| async_tree_memoization_tg        | 240 ms                                                     | 259 ms: 1.08x slower                                                   |
| coroutines                       | 15.8 ms                                                    | 17.2 ms: 1.08x slower                                                  |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.02 ms: 1.09x slower                                                  |
| nbody                            | 59.6 ms                                                    | 65.2 ms: 1.09x slower                                                  |
| tornado_http                     | 66.7 ms                                                    | 75.0 ms: 1.12x slower                                                  |
| generators                       | 22.9 ms                                                    | 28.9 ms: 1.26x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                           |

Benchmark hidden because not significant (18): async_tree_io_tg, async_tree_eager_io_tg, dask, async_tree_cpu_io_mixed, async_tree_none_tg, pylint, 2to3, go, regex_dna, mdp, pidigits, mypy2, dulwich_log, async_tree_io, asyncio_tcp, unpickle, async_tree_eager_memoization, async_tree_eager_io
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.97x