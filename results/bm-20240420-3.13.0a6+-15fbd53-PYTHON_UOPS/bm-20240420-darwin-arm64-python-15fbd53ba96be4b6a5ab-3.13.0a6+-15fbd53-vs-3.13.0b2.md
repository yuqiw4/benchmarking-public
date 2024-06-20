# Results vs. 3.13.0b2

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 172 ms: 1.07x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.68 ms: 1.10x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.57 sec: 1.09x slower                                                 |
| html5lib       | 31.2 ms                                                    | 32.2 ms: 1.03x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 78.8 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                      | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 337 ms: 1.02x slower                                                   |
| async_tree_io                    | 563 ms                                                     | 576 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 368 ms: 1.03x slower                                                   |
| async_tree_eager_io              | 766 ms                                                     | 789 ms: 1.03x slower                                                   |
| async_tree_none_tg               | 198 ms                                                     | 204 ms: 1.03x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 470 ms: 1.04x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 133 ms: 1.06x slower                                                   |
| async_tree_memoization           | 260 ms                                                     | 280 ms: 1.08x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 45.4 ms: 1.10x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 265 ms: 1.11x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 68.6 ms: 1.14x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.04x slower                                                           |

Benchmark hidden because not significant (5): async_tree_eager_io_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| float          | 48.6 ms                                                    | 64.7 ms: 1.33x slower                                                  |
| nbody          | 59.6 ms                                                    | 83.4 ms: 1.40x slower                                                  |
| Geometric mean | (ref)                                                      | 1.23x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 149 ms                                                     | 149 ms: 1.00x faster                                                   |
| regex_effbot   | 2.58 ms                                                    | 2.63 ms: 1.02x slower                                                  |
| regex_v8       | 17.3 ms                                                    | 17.6 ms: 1.02x slower                                                  |
| regex_compile  | 68.5 ms                                                    | 92.8 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                      | 1.09x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 106 ms                                                     | 99.0 ms: 1.07x faster                                                  |
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| json_loads           | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| unpickle             | 9.12 us                                                    | 9.21 us: 1.01x slower                                                  |
| unpickle_list        | 2.88 us                                                    | 2.91 us: 1.01x slower                                                  |
| pickle_list          | 2.96 us                                                    | 3.02 us: 1.02x slower                                                  |
| xml_etree_iterparse  | 71.5 ms                                                    | 73.0 ms: 1.02x slower                                                  |
| json_dumps           | 6.23 ms                                                    | 6.39 ms: 1.03x slower                                                  |
| pickle_pure_python   | 179 us                                                     | 184 us: 1.03x slower                                                   |
| xml_etree_process    | 37.1 ms                                                    | 39.1 ms: 1.06x slower                                                  |
| xml_etree_generate   | 52.7 ms                                                    | 56.8 ms: 1.08x slower                                                  |
| tomli_loads          | 1.47 sec                                                   | 1.66 sec: 1.13x slower                                                 |
| unpickle_pure_python | 141 us                                                     | 181 us: 1.29x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.04x slower                                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 12.3 ms                                                    | 9.19 ms: 1.34x faster                                                  |
| python_startup         | 15.2 ms                                                    | 12.0 ms: 1.26x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.30x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 29.9 ms                                                    | 32.0 ms: 1.07x slower                                                  |
| genshi_text     | 13.9 ms                                                    | 15.0 ms: 1.08x slower                                                  |
| django_template | 19.4 ms                                                    | 22.3 ms: 1.15x slower                                                  |
| mako            | 6.99 ms                                                    | 9.33 ms: 1.34x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.15x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site           | 12.3 ms                                                    | 9.19 ms: 1.34x faster                                                  |
| python_startup                   | 15.2 ms                                                    | 12.0 ms: 1.26x faster                                                  |
| typing_runtime_protocols         | 87.6 us                                                    | 71.2 us: 1.23x faster                                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 43.6 ms: 1.08x faster                                                  |
| xml_etree_parse                  | 106 ms                                                     | 99.0 ms: 1.07x faster                                                  |
| create_gc_cycles                 | 897 us                                                     | 877 us: 1.02x faster                                                   |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| regex_dna                        | 149 ms                                                     | 149 ms: 1.00x faster                                                   |
| gc_traversal                     | 2.45 ms                                                    | 2.45 ms: 1.00x slower                                                  |
| pidigits                         | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| unpickle                         | 9.12 us                                                    | 9.21 us: 1.01x slower                                                  |
| unpickle_list                    | 2.88 us                                                    | 2.91 us: 1.01x slower                                                  |
| regex_effbot                     | 2.58 ms                                                    | 2.63 ms: 1.02x slower                                                  |
| regex_v8                         | 17.3 ms                                                    | 17.6 ms: 1.02x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 337 ms: 1.02x slower                                                   |
| thrift                           | 435 us                                                     | 443 us: 1.02x slower                                                   |
| pickle_list                      | 2.96 us                                                    | 3.02 us: 1.02x slower                                                  |
| xml_etree_iterparse              | 71.5 ms                                                    | 73.0 ms: 1.02x slower                                                  |
| async_tree_io                    | 563 ms                                                     | 576 ms: 1.02x slower                                                   |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.32 sec: 1.02x slower                                                 |
| telco                            | 4.60 ms                                                    | 4.72 ms: 1.02x slower                                                  |
| json_dumps                       | 6.23 ms                                                    | 6.39 ms: 1.03x slower                                                  |
| coverage                         | 45.0 ms                                                    | 46.2 ms: 1.03x slower                                                  |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 368 ms: 1.03x slower                                                   |
| async_tree_eager_io              | 766 ms                                                     | 789 ms: 1.03x slower                                                   |
| pickle_pure_python               | 179 us                                                     | 184 us: 1.03x slower                                                   |
| pathlib                          | 23.3 ms                                                    | 24.0 ms: 1.03x slower                                                  |
| async_tree_none_tg               | 198 ms                                                     | 204 ms: 1.03x slower                                                   |
| html5lib                         | 31.2 ms                                                    | 32.2 ms: 1.03x slower                                                  |
| deepcopy_reduce                  | 1.82 us                                                    | 1.90 us: 1.04x slower                                                  |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 470 ms: 1.04x slower                                                   |
| async_generators                 | 281 ms                                                     | 294 ms: 1.04x slower                                                   |
| logging_format                   | 3.31 us                                                    | 3.47 us: 1.05x slower                                                  |
| dulwich_log                      | 27.6 ms                                                    | 28.9 ms: 1.05x slower                                                  |
| sqlite_synth                     | 1.55 us                                                    | 1.63 us: 1.05x slower                                                  |
| mdp                              | 1.53 sec                                                   | 1.61 sec: 1.05x slower                                                 |
| xml_etree_process                | 37.1 ms                                                    | 39.1 ms: 1.06x slower                                                  |
| logging_simple                   | 3.04 us                                                    | 3.21 us: 1.06x slower                                                  |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 133 ms: 1.06x slower                                                   |
| coroutines                       | 15.8 ms                                                    | 16.8 ms: 1.06x slower                                                  |
| pycparser                        | 632 ms                                                     | 672 ms: 1.06x slower                                                   |
| genshi_xml                       | 29.9 ms                                                    | 32.0 ms: 1.07x slower                                                  |
| 2to3                             | 161 ms                                                     | 172 ms: 1.07x slower                                                   |
| deepcopy                         | 204 us                                                     | 219 us: 1.08x slower                                                   |
| mypy2                            | 379 ms                                                     | 408 ms: 1.08x slower                                                   |
| xml_etree_generate               | 52.7 ms                                                    | 56.8 ms: 1.08x slower                                                  |
| async_tree_memoization           | 260 ms                                                     | 280 ms: 1.08x slower                                                   |
| genshi_text                      | 13.9 ms                                                    | 15.0 ms: 1.08x slower                                                  |
| sympy_expand                     | 226 ms                                                     | 244 ms: 1.08x slower                                                   |
| docutils                         | 1.44 sec                                                   | 1.57 sec: 1.09x slower                                                 |
| logging_silent                   | 60.1 ns                                                    | 65.6 ns: 1.09x slower                                                  |
| sqlglot_normalize                | 166 ms                                                     | 181 ms: 1.10x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 45.4 ms: 1.10x slower                                                  |
| chameleon                        | 4.27 ms                                                    | 4.68 ms: 1.10x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 265 ms: 1.11x slower                                                   |
| richards_super                   | 35.2 ms                                                    | 39.0 ms: 1.11x slower                                                  |
| richards                         | 31.8 ms                                                    | 35.4 ms: 1.11x slower                                                  |
| meteor_contest                   | 70.3 ms                                                    | 78.9 ms: 1.12x slower                                                  |
| sqlglot_transpile                | 891 us                                                     | 1.00 ms: 1.12x slower                                                  |
| bench_thread_pool                | 447 us                                                     | 503 us: 1.13x slower                                                   |
| tomli_loads                      | 1.47 sec                                                   | 1.66 sec: 1.13x slower                                                 |
| generators                       | 22.9 ms                                                    | 26.0 ms: 1.14x slower                                                  |
| sympy_integrate                  | 10.3 ms                                                    | 11.8 ms: 1.14x slower                                                  |
| async_tree_eager                 | 60.3 ms                                                    | 68.6 ms: 1.14x slower                                                  |
| sqlglot_parse                    | 732 us                                                     | 833 us: 1.14x slower                                                   |
| sqlglot_optimize                 | 30.9 ms                                                    | 35.2 ms: 1.14x slower                                                  |
| crypto_pyaes                     | 49.5 ms                                                    | 56.6 ms: 1.14x slower                                                  |
| django_template                  | 19.4 ms                                                    | 22.3 ms: 1.15x slower                                                  |
| gunicorn                         | 1.04 ms                                                    | 1.19 ms: 1.15x slower                                                  |
| sympy_str                        | 131 ms                                                     | 151 ms: 1.15x slower                                                   |
| aiohttp                          | 997 us                                                     | 1.15 ms: 1.15x slower                                                  |
| sympy_sum                        | 69.2 ms                                                    | 81.0 ms: 1.17x slower                                                  |
| go                               | 101 ms                                                     | 119 ms: 1.18x slower                                                   |
| scimark_sor                      | 94.9 ms                                                    | 112 ms: 1.18x slower                                                   |
| tornado_http                     | 66.7 ms                                                    | 78.8 ms: 1.18x slower                                                  |
| deepcopy_memo                    | 22.6 us                                                    | 27.3 us: 1.21x slower                                                  |
| raytrace                         | 147 ms                                                     | 181 ms: 1.23x slower                                                   |
| pprint_safe_repr                 | 465 ms                                                     | 587 ms: 1.26x slower                                                   |
| pprint_pformat                   | 947 ms                                                     | 1.20 sec: 1.27x slower                                                 |
| unpickle_pure_python             | 141 us                                                     | 181 us: 1.29x slower                                                   |
| pyflate                          | 321 ms                                                     | 418 ms: 1.30x slower                                                   |
| deltablue                        | 2.14 ms                                                    | 2.81 ms: 1.31x slower                                                  |
| float                            | 48.6 ms                                                    | 64.7 ms: 1.33x slower                                                  |
| mako                             | 6.99 ms                                                    | 9.33 ms: 1.34x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 69.9 ms: 1.34x slower                                                  |
| regex_compile                    | 68.5 ms                                                    | 92.8 ms: 1.35x slower                                                  |
| scimark_fft                      | 181 ms                                                     | 246 ms: 1.36x slower                                                   |
| fannkuch                         | 248 ms                                                     | 341 ms: 1.37x slower                                                   |
| nbody                            | 59.6 ms                                                    | 83.4 ms: 1.40x slower                                                  |
| chaos                            | 34.0 ms                                                    | 48.4 ms: 1.42x slower                                                  |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 4.00 ms: 1.44x slower                                                  |
| hexiom                           | 4.06 ms                                                    | 5.96 ms: 1.47x slower                                                  |
| scimark_lu                       | 66.9 ms                                                    | 101 ms: 1.51x slower                                                   |
| spectral_norm                    | 66.4 ms                                                    | 100 ms: 1.51x slower                                                   |
| scimark_monte_carlo              | 42.5 ms                                                    | 64.3 ms: 1.51x slower                                                  |
| comprehensions                   | 10.2 us                                                    | 16.5 us: 1.63x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.10x slower                                                           |

Benchmark hidden because not significant (11): asyncio_tcp, pickle, asyncio_websockets, json, dask, async_tree_eager_io_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_eager_memoization, pylint
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 0.97x