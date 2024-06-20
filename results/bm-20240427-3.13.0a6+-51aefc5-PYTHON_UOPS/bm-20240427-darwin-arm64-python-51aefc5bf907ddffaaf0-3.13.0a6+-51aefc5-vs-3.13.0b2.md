# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: darwin-arm64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.13x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 180 ms: 1.12x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.76 ms: 1.12x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.60 sec: 1.11x slower                                                 |
| html5lib       | 31.2 ms                                                    | 32.2 ms: 1.03x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 78.6 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                      | 1.11x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 338 ms: 1.02x slower                                                   |
| async_tree_io                    | 563 ms                                                     | 579 ms: 1.03x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 370 ms: 1.03x slower                                                   |
| async_tree_eager_io              | 766 ms                                                     | 792 ms: 1.03x slower                                                   |
| async_tree_none_tg               | 198 ms                                                     | 205 ms: 1.04x slower                                                   |
| async_tree_eager_memoization     | 152 ms                                                     | 159 ms: 1.05x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 474 ms: 1.05x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 134 ms: 1.07x slower                                                   |
| async_tree_memoization           | 260 ms                                                     | 280 ms: 1.08x slower                                                   |
| async_tree_memoization_tg        | 240 ms                                                     | 268 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 46.2 ms: 1.12x slower                                                  |
| async_tree_eager                 | 60.3 ms                                                    | 69.6 ms: 1.15x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.05x slower                                                           |

Benchmark hidden because not significant (4): async_tree_eager_io_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| float          | 48.6 ms                                                    | 65.0 ms: 1.34x slower                                                  |
| nbody          | 59.6 ms                                                    | 84.1 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                      | 1.24x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 2.58 ms                                                    | 2.57 ms: 1.01x faster                                                  |
| regex_dna      | 149 ms                                                     | 149 ms: 1.00x faster                                                   |
| regex_v8       | 17.3 ms                                                    | 17.7 ms: 1.02x slower                                                  |
| regex_compile  | 68.5 ms                                                    | 95.1 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                      | 1.09x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| json_loads           | 16.8 us                                                    | 16.9 us: 1.01x slower                                                  |
| json_dumps           | 6.23 ms                                                    | 6.31 ms: 1.01x slower                                                  |
| unpickle             | 9.12 us                                                    | 9.26 us: 1.01x slower                                                  |
| unpickle_list        | 2.88 us                                                    | 2.93 us: 1.01x slower                                                  |
| pickle_pure_python   | 179 us                                                     | 188 us: 1.05x slower                                                   |
| xml_etree_process    | 37.1 ms                                                    | 40.0 ms: 1.08x slower                                                  |
| xml_etree_iterparse  | 71.5 ms                                                    | 77.4 ms: 1.08x slower                                                  |
| xml_etree_generate   | 52.7 ms                                                    | 58.2 ms: 1.10x slower                                                  |
| tomli_loads          | 1.47 sec                                                   | 1.64 sec: 1.12x slower                                                 |
| unpickle_pure_python | 141 us                                                     | 182 us: 1.29x slower                                                   |
| Geometric mean       | (ref)                                                      | 1.05x slower                                                           |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 12.3 ms                                                    | 10.9 ms: 1.13x faster                                                  |
| python_startup         | 15.2 ms                                                    | 13.6 ms: 1.11x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.12x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 29.9 ms                                                    | 34.6 ms: 1.16x slower                                                  |
| django_template | 19.4 ms                                                    | 23.1 ms: 1.19x slower                                                  |
| genshi_text     | 13.9 ms                                                    | 16.7 ms: 1.20x slower                                                  |
| mako            | 6.99 ms                                                    | 9.31 ms: 1.33x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.22x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site           | 12.3 ms                                                    | 10.9 ms: 1.13x faster                                                  |
| python_startup                   | 15.2 ms                                                    | 13.6 ms: 1.11x faster                                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 44.9 ms: 1.05x faster                                                  |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| regex_effbot                     | 2.58 ms                                                    | 2.57 ms: 1.01x faster                                                  |
| coverage                         | 45.0 ms                                                    | 44.8 ms: 1.00x faster                                                  |
| regex_dna                        | 149 ms                                                     | 149 ms: 1.00x faster                                                   |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                   |
| pidigits                         | 282 ms                                                     | 283 ms: 1.00x slower                                                   |
| gc_traversal                     | 2.45 ms                                                    | 2.46 ms: 1.00x slower                                                  |
| json_loads                       | 16.8 us                                                    | 16.9 us: 1.01x slower                                                  |
| telco                            | 4.60 ms                                                    | 4.64 ms: 1.01x slower                                                  |
| create_gc_cycles                 | 897 us                                                     | 905 us: 1.01x slower                                                   |
| json_dumps                       | 6.23 ms                                                    | 6.31 ms: 1.01x slower                                                  |
| unpickle                         | 9.12 us                                                    | 9.26 us: 1.01x slower                                                  |
| unpickle_list                    | 2.88 us                                                    | 2.93 us: 1.01x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 338 ms: 1.02x slower                                                   |
| regex_v8                         | 17.3 ms                                                    | 17.7 ms: 1.02x slower                                                  |
| dask                             | 221 ms                                                     | 227 ms: 1.02x slower                                                   |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.32 sec: 1.03x slower                                                 |
| async_tree_io                    | 563 ms                                                     | 579 ms: 1.03x slower                                                   |
| thrift                           | 435 us                                                     | 449 us: 1.03x slower                                                   |
| html5lib                         | 31.2 ms                                                    | 32.2 ms: 1.03x slower                                                  |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 370 ms: 1.03x slower                                                   |
| async_tree_eager_io              | 766 ms                                                     | 792 ms: 1.03x slower                                                   |
| pathlib                          | 23.3 ms                                                    | 24.2 ms: 1.04x slower                                                  |
| async_tree_none_tg               | 198 ms                                                     | 205 ms: 1.04x slower                                                   |
| sqlite_synth                     | 1.55 us                                                    | 1.62 us: 1.04x slower                                                  |
| async_tree_eager_memoization     | 152 ms                                                     | 159 ms: 1.05x slower                                                   |
| deepcopy_reduce                  | 1.82 us                                                    | 1.91 us: 1.05x slower                                                  |
| coroutines                       | 15.8 ms                                                    | 16.6 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 474 ms: 1.05x slower                                                   |
| pickle_pure_python               | 179 us                                                     | 188 us: 1.05x slower                                                   |
| async_generators                 | 281 ms                                                     | 296 ms: 1.06x slower                                                   |
| dulwich_log                      | 27.6 ms                                                    | 29.3 ms: 1.06x slower                                                  |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 134 ms: 1.07x slower                                                   |
| pycparser                        | 632 ms                                                     | 678 ms: 1.07x slower                                                   |
| async_tree_memoization           | 260 ms                                                     | 280 ms: 1.08x slower                                                   |
| xml_etree_process                | 37.1 ms                                                    | 40.0 ms: 1.08x slower                                                  |
| xml_etree_iterparse              | 71.5 ms                                                    | 77.4 ms: 1.08x slower                                                  |
| sympy_expand                     | 226 ms                                                     | 245 ms: 1.09x slower                                                   |
| logging_format                   | 3.31 us                                                    | 3.60 us: 1.09x slower                                                  |
| pylint                           | 170 ms                                                     | 185 ms: 1.09x slower                                                   |
| logging_simple                   | 3.04 us                                                    | 3.32 us: 1.09x slower                                                  |
| mdp                              | 1.53 sec                                                   | 1.68 sec: 1.10x slower                                                 |
| deepcopy                         | 204 us                                                     | 225 us: 1.10x slower                                                   |
| xml_etree_generate               | 52.7 ms                                                    | 58.2 ms: 1.10x slower                                                  |
| logging_silent                   | 60.1 ns                                                    | 66.6 ns: 1.11x slower                                                  |
| richards_super                   | 35.2 ms                                                    | 39.0 ms: 1.11x slower                                                  |
| docutils                         | 1.44 sec                                                   | 1.60 sec: 1.11x slower                                                 |
| richards                         | 31.8 ms                                                    | 35.5 ms: 1.11x slower                                                  |
| chameleon                        | 4.27 ms                                                    | 4.76 ms: 1.12x slower                                                  |
| 2to3                             | 161 ms                                                     | 180 ms: 1.12x slower                                                   |
| async_tree_memoization_tg        | 240 ms                                                     | 268 ms: 1.12x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 46.2 ms: 1.12x slower                                                  |
| aiohttp                          | 997 us                                                     | 1.11 ms: 1.12x slower                                                  |
| tomli_loads                      | 1.47 sec                                                   | 1.64 sec: 1.12x slower                                                 |
| sqlglot_transpile                | 891 us                                                     | 1.01 ms: 1.13x slower                                                  |
| sqlglot_parse                    | 732 us                                                     | 832 us: 1.14x slower                                                   |
| crypto_pyaes                     | 49.5 ms                                                    | 56.4 ms: 1.14x slower                                                  |
| sqlglot_normalize                | 166 ms                                                     | 189 ms: 1.14x slower                                                   |
| meteor_contest                   | 70.3 ms                                                    | 80.5 ms: 1.15x slower                                                  |
| sympy_integrate                  | 10.3 ms                                                    | 11.9 ms: 1.15x slower                                                  |
| bench_thread_pool                | 447 us                                                     | 516 us: 1.15x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 69.6 ms: 1.15x slower                                                  |
| genshi_xml                       | 29.9 ms                                                    | 34.6 ms: 1.16x slower                                                  |
| gunicorn                         | 1.04 ms                                                    | 1.20 ms: 1.16x slower                                                  |
| sqlglot_optimize                 | 30.9 ms                                                    | 36.2 ms: 1.17x slower                                                  |
| sympy_str                        | 131 ms                                                     | 154 ms: 1.17x slower                                                   |
| scimark_sor                      | 94.9 ms                                                    | 111 ms: 1.17x slower                                                   |
| tornado_http                     | 66.7 ms                                                    | 78.6 ms: 1.18x slower                                                  |
| go                               | 101 ms                                                     | 119 ms: 1.18x slower                                                   |
| generators                       | 22.9 ms                                                    | 27.1 ms: 1.18x slower                                                  |
| django_template                  | 19.4 ms                                                    | 23.1 ms: 1.19x slower                                                  |
| sympy_sum                        | 69.2 ms                                                    | 82.3 ms: 1.19x slower                                                  |
| genshi_text                      | 13.9 ms                                                    | 16.7 ms: 1.20x slower                                                  |
| deepcopy_memo                    | 22.6 us                                                    | 27.7 us: 1.23x slower                                                  |
| raytrace                         | 147 ms                                                     | 183 ms: 1.24x slower                                                   |
| typing_runtime_protocols         | 87.6 us                                                    | 111 us: 1.26x slower                                                   |
| pprint_safe_repr                 | 465 ms                                                     | 593 ms: 1.28x slower                                                   |
| pprint_pformat                   | 947 ms                                                     | 1.21 sec: 1.28x slower                                                 |
| pyflate                          | 321 ms                                                     | 411 ms: 1.28x slower                                                   |
| unpickle_pure_python             | 141 us                                                     | 182 us: 1.29x slower                                                   |
| scimark_fft                      | 181 ms                                                     | 236 ms: 1.31x slower                                                   |
| fannkuch                         | 248 ms                                                     | 325 ms: 1.31x slower                                                   |
| mypy2                            | 379 ms                                                     | 502 ms: 1.32x slower                                                   |
| mako                             | 6.99 ms                                                    | 9.31 ms: 1.33x slower                                                  |
| deltablue                        | 2.14 ms                                                    | 2.86 ms: 1.34x slower                                                  |
| float                            | 48.6 ms                                                    | 65.0 ms: 1.34x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 72.1 ms: 1.38x slower                                                  |
| regex_compile                    | 68.5 ms                                                    | 95.1 ms: 1.39x slower                                                  |
| chaos                            | 34.0 ms                                                    | 47.8 ms: 1.41x slower                                                  |
| nbody                            | 59.6 ms                                                    | 84.1 ms: 1.41x slower                                                  |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.92 ms: 1.41x slower                                                  |
| spectral_norm                    | 66.4 ms                                                    | 95.2 ms: 1.43x slower                                                  |
| scimark_monte_carlo              | 42.5 ms                                                    | 63.6 ms: 1.50x slower                                                  |
| hexiom                           | 4.06 ms                                                    | 6.19 ms: 1.53x slower                                                  |
| scimark_lu                       | 66.9 ms                                                    | 103 ms: 1.54x slower                                                   |
| comprehensions                   | 10.2 us                                                    | 17.9 us: 1.77x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.13x slower                                                           |

Benchmark hidden because not significant (9): xml_etree_parse, async_tree_eager_io_tg, pickle_list, pickle, json, async_tree_none, async_tree_cpu_io_mixed, async_tree_io_tg, asyncio_tcp
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 0.97x