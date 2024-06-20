# Results vs. 3.13.0b2

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: darwin-arm64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 180 ms: 1.12x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.54 ms: 1.06x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.45 sec: 1.01x slower                                                 |
| html5lib       | 31.2 ms                                                    | 31.9 ms: 1.02x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 76.6 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                      | 1.07x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none                  | 209 ms                                                     | 203 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 364 ms: 1.02x slower                                                   |
| async_tree_memoization           | 260 ms                                                     | 270 ms: 1.04x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 469 ms: 1.04x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.04x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 62.8 ms: 1.04x slower                                                  |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.4 ms: 1.05x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 261 ms: 1.09x slower                                                   |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                           |

Benchmark hidden because not significant (7): async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_eager_memoization, async_tree_none_tg, async_tree_eager_io, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 48.6 ms                                                    | 52.0 ms: 1.07x slower                                                  |
| nbody          | 59.6 ms                                                    | 69.7 ms: 1.17x slower                                                  |
| Geometric mean | (ref)                                                      | 1.08x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 149 ms                                                     | 150 ms: 1.00x slower                                                   |
| regex_v8       | 17.3 ms                                                    | 17.4 ms: 1.01x slower                                                  |
| regex_compile  | 68.5 ms                                                    | 69.6 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|---------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 106 ms                                                     | 104 ms: 1.02x faster                                                   |
| pickle              | 7.48 us                                                    | 7.45 us: 1.00x faster                                                  |
| json_loads          | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| unpickle            | 9.12 us                                                    | 9.22 us: 1.01x slower                                                  |
| xml_etree_iterparse | 71.5 ms                                                    | 72.5 ms: 1.01x slower                                                  |
| xml_etree_process   | 37.1 ms                                                    | 37.6 ms: 1.02x slower                                                  |
| unpickle_list       | 2.88 us                                                    | 2.95 us: 1.02x slower                                                  |
| tomli_loads         | 1.47 sec                                                   | 1.51 sec: 1.03x slower                                                 |
| pickle_pure_python  | 179 us                                                     | 184 us: 1.03x slower                                                   |
| xml_etree_generate  | 52.7 ms                                                    | 55.1 ms: 1.05x slower                                                  |
| Geometric mean      | (ref)                                                      | 1.01x slower                                                           |

Benchmark hidden because not significant (4): json_dumps, pickle_dict, pickle_list, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 12.3 ms                                                    | 10.8 ms: 1.14x faster                                                  |
| python_startup         | 15.2 ms                                                    | 13.6 ms: 1.12x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.13x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 6.99 ms                                                    | 7.09 ms: 1.01x slower                                                  |
| django_template | 19.4 ms                                                    | 20.2 ms: 1.04x slower                                                  |
| genshi_xml      | 29.9 ms                                                    | 31.4 ms: 1.05x slower                                                  |
| genshi_text     | 13.9 ms                                                    | 15.0 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                      | 1.05x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240427-darwin-arm64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site           | 12.3 ms                                                    | 10.8 ms: 1.14x faster                                                  |
| python_startup                   | 15.2 ms                                                    | 13.6 ms: 1.12x faster                                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 44.0 ms: 1.07x faster                                                  |
| crypto_pyaes                     | 49.5 ms                                                    | 47.3 ms: 1.05x faster                                                  |
| async_tree_none                  | 209 ms                                                     | 203 ms: 1.03x faster                                                   |
| telco                            | 4.60 ms                                                    | 4.47 ms: 1.03x faster                                                  |
| xml_etree_parse                  | 106 ms                                                     | 104 ms: 1.02x faster                                                   |
| json                             | 2.93 ms                                                    | 2.91 ms: 1.01x faster                                                  |
| pickle                           | 7.48 us                                                    | 7.45 us: 1.00x faster                                                  |
| coverage                         | 45.0 ms                                                    | 44.8 ms: 1.00x faster                                                  |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                   |
| gc_traversal                     | 2.45 ms                                                    | 2.46 ms: 1.00x slower                                                  |
| regex_dna                        | 149 ms                                                     | 150 ms: 1.00x slower                                                   |
| create_gc_cycles                 | 897 us                                                     | 903 us: 1.01x slower                                                   |
| sympy_integrate                  | 10.3 ms                                                    | 10.4 ms: 1.01x slower                                                  |
| richards_super                   | 35.2 ms                                                    | 35.5 ms: 1.01x slower                                                  |
| regex_v8                         | 17.3 ms                                                    | 17.4 ms: 1.01x slower                                                  |
| go                               | 101 ms                                                     | 102 ms: 1.01x slower                                                   |
| pyflate                          | 321 ms                                                     | 324 ms: 1.01x slower                                                   |
| json_loads                       | 16.8 us                                                    | 17.0 us: 1.01x slower                                                  |
| unpickle                         | 9.12 us                                                    | 9.22 us: 1.01x slower                                                  |
| richards                         | 31.8 ms                                                    | 32.2 ms: 1.01x slower                                                  |
| docutils                         | 1.44 sec                                                   | 1.45 sec: 1.01x slower                                                 |
| pycparser                        | 632 ms                                                     | 641 ms: 1.01x slower                                                   |
| dulwich_log                      | 27.6 ms                                                    | 27.9 ms: 1.01x slower                                                  |
| xml_etree_iterparse              | 71.5 ms                                                    | 72.5 ms: 1.01x slower                                                  |
| sympy_expand                     | 226 ms                                                     | 229 ms: 1.01x slower                                                   |
| mako                             | 6.99 ms                                                    | 7.09 ms: 1.01x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 336 ms: 1.01x slower                                                   |
| xml_etree_process                | 37.1 ms                                                    | 37.6 ms: 1.02x slower                                                  |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 364 ms: 1.02x slower                                                   |
| regex_compile                    | 68.5 ms                                                    | 69.6 ms: 1.02x slower                                                  |
| thrift                           | 435 us                                                     | 443 us: 1.02x slower                                                   |
| sympy_str                        | 131 ms                                                     | 134 ms: 1.02x slower                                                   |
| meteor_contest                   | 70.3 ms                                                    | 71.7 ms: 1.02x slower                                                  |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.32 sec: 1.02x slower                                                 |
| async_generators                 | 281 ms                                                     | 287 ms: 1.02x slower                                                   |
| html5lib                         | 31.2 ms                                                    | 31.9 ms: 1.02x slower                                                  |
| sympy_sum                        | 69.2 ms                                                    | 70.9 ms: 1.02x slower                                                  |
| unpickle_list                    | 2.88 us                                                    | 2.95 us: 1.02x slower                                                  |
| fannkuch                         | 248 ms                                                     | 256 ms: 1.03x slower                                                   |
| comprehensions                   | 10.2 us                                                    | 10.5 us: 1.03x slower                                                  |
| tomli_loads                      | 1.47 sec                                                   | 1.51 sec: 1.03x slower                                                 |
| pathlib                          | 23.3 ms                                                    | 24.0 ms: 1.03x slower                                                  |
| deltablue                        | 2.14 ms                                                    | 2.21 ms: 1.03x slower                                                  |
| pickle_pure_python               | 179 us                                                     | 184 us: 1.03x slower                                                   |
| deepcopy_reduce                  | 1.82 us                                                    | 1.88 us: 1.04x slower                                                  |
| scimark_lu                       | 66.9 ms                                                    | 69.5 ms: 1.04x slower                                                  |
| async_tree_memoization           | 260 ms                                                     | 270 ms: 1.04x slower                                                   |
| async_tree_cpu_io_mixed_tg       | 451 ms                                                     | 469 ms: 1.04x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.04x slower                                                   |
| sqlglot_optimize                 | 30.9 ms                                                    | 32.2 ms: 1.04x slower                                                  |
| sqlglot_normalize                | 166 ms                                                     | 173 ms: 1.04x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 62.8 ms: 1.04x slower                                                  |
| sqlglot_transpile                | 891 us                                                     | 928 us: 1.04x slower                                                   |
| django_template                  | 19.4 ms                                                    | 20.2 ms: 1.04x slower                                                  |
| pprint_pformat                   | 947 ms                                                     | 988 ms: 1.04x slower                                                   |
| deepcopy                         | 204 us                                                     | 213 us: 1.04x slower                                                   |
| pprint_safe_repr                 | 465 ms                                                     | 485 ms: 1.04x slower                                                   |
| sqlglot_parse                    | 732 us                                                     | 765 us: 1.04x slower                                                   |
| logging_format                   | 3.31 us                                                    | 3.46 us: 1.04x slower                                                  |
| xml_etree_generate               | 52.7 ms                                                    | 55.1 ms: 1.05x slower                                                  |
| logging_simple                   | 3.04 us                                                    | 3.18 us: 1.05x slower                                                  |
| hexiom                           | 4.06 ms                                                    | 4.25 ms: 1.05x slower                                                  |
| scimark_sor                      | 94.9 ms                                                    | 99.3 ms: 1.05x slower                                                  |
| deepcopy_memo                    | 22.6 us                                                    | 23.6 us: 1.05x slower                                                  |
| genshi_xml                       | 29.9 ms                                                    | 31.4 ms: 1.05x slower                                                  |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.4 ms: 1.05x slower                                                  |
| raytrace                         | 147 ms                                                     | 154 ms: 1.05x slower                                                   |
| bench_thread_pool                | 447 us                                                     | 470 us: 1.05x slower                                                   |
| chameleon                        | 4.27 ms                                                    | 4.54 ms: 1.06x slower                                                  |
| scimark_monte_carlo              | 42.5 ms                                                    | 45.2 ms: 1.06x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 55.6 ms: 1.07x slower                                                  |
| coroutines                       | 15.8 ms                                                    | 16.9 ms: 1.07x slower                                                  |
| float                            | 48.6 ms                                                    | 52.0 ms: 1.07x slower                                                  |
| chaos                            | 34.0 ms                                                    | 36.5 ms: 1.07x slower                                                  |
| logging_silent                   | 60.1 ns                                                    | 64.9 ns: 1.08x slower                                                  |
| aiohttp                          | 997 us                                                     | 1.08 ms: 1.08x slower                                                  |
| genshi_text                      | 13.9 ms                                                    | 15.0 ms: 1.08x slower                                                  |
| gunicorn                         | 1.04 ms                                                    | 1.12 ms: 1.08x slower                                                  |
| typing_runtime_protocols         | 87.6 us                                                    | 94.9 us: 1.08x slower                                                  |
| spectral_norm                    | 66.4 ms                                                    | 72.1 ms: 1.09x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 261 ms: 1.09x slower                                                   |
| scimark_fft                      | 181 ms                                                     | 199 ms: 1.10x slower                                                   |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.07 ms: 1.11x slower                                                  |
| 2to3                             | 161 ms                                                     | 180 ms: 1.12x slower                                                   |
| tornado_http                     | 66.7 ms                                                    | 76.6 ms: 1.15x slower                                                  |
| nbody                            | 59.6 ms                                                    | 69.7 ms: 1.17x slower                                                  |
| mypy2                            | 379 ms                                                     | 464 ms: 1.22x slower                                                   |
| generators                       | 22.9 ms                                                    | 28.3 ms: 1.24x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.03x slower                                                           |

Benchmark hidden because not significant (18): async_tree_eager_io_tg, async_tree_cpu_io_mixed, dask, regex_effbot, pidigits, json_dumps, pickle_dict, pickle_list, unpickle_pure_python, mdp, async_tree_io_tg, sqlite_synth, async_tree_eager_memoization, async_tree_none_tg, pylint, async_tree_eager_io, async_tree_io, asyncio_tcp
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.97x