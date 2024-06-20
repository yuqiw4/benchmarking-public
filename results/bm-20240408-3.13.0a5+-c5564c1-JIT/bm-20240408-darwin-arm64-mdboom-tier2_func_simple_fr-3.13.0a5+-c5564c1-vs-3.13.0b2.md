# Results vs. 3.13.0b2

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: darwin-arm64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.04x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 161 ms                                                     | 171 ms: 1.07x slower                                                   |
| chameleon      | 4.27 ms                                                    | 4.46 ms: 1.04x slower                                                  |
| docutils       | 1.44 sec                                                   | 1.55 sec: 1.08x slower                                                 |
| html5lib       | 31.2 ms                                                    | 32.8 ms: 1.05x slower                                                  |
| tornado_http   | 66.7 ms                                                    | 82.6 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                      | 1.09x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none                  | 209 ms                                                     | 202 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 335 ms: 1.01x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 365 ms: 1.02x slower                                                   |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.05x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.3 ms: 1.05x slower                                                  |
| async_tree_eager                 | 60.3 ms                                                    | 65.1 ms: 1.08x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 260 ms: 1.09x slower                                                   |
| Geometric mean                   | (ref)                                                      | 1.02x slower                                                           |

Benchmark hidden because not significant (9): async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_none_tg, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_eager_io, async_tree_memoization, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 282 ms                                                     | 282 ms: 1.00x slower                                                   |
| float          | 48.6 ms                                                    | 49.2 ms: 1.01x slower                                                  |
| nbody          | 59.6 ms                                                    | 70.6 ms: 1.18x slower                                                  |
| Geometric mean | (ref)                                                      | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 17.3 ms                                                    | 17.1 ms: 1.01x faster                                                  |
| regex_effbot   | 2.58 ms                                                    | 2.64 ms: 1.02x slower                                                  |
| regex_dna      | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| regex_compile  | 68.5 ms                                                    | 85.3 ms: 1.24x slower                                                  |
| Geometric mean | (ref)                                                      | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|---------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads         | 1.47 sec                                                   | 1.28 sec: 1.15x faster                                                 |
| xml_etree_parse     | 106 ms                                                     | 98.5 ms: 1.07x faster                                                  |
| xml_etree_iterparse | 71.5 ms                                                    | 68.5 ms: 1.04x faster                                                  |
| pickle              | 7.48 us                                                    | 7.25 us: 1.03x faster                                                  |
| pickle_dict         | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| json_loads          | 16.8 us                                                    | 16.9 us: 1.00x slower                                                  |
| xml_etree_process   | 37.1 ms                                                    | 37.3 ms: 1.01x slower                                                  |
| json_dumps          | 6.23 ms                                                    | 6.32 ms: 1.01x slower                                                  |
| unpickle            | 9.12 us                                                    | 9.27 us: 1.02x slower                                                  |
| pickle_pure_python  | 179 us                                                     | 182 us: 1.02x slower                                                   |
| xml_etree_generate  | 52.7 ms                                                    | 54.4 ms: 1.03x slower                                                  |
| unpickle_list       | 2.88 us                                                    | 2.99 us: 1.04x slower                                                  |
| Geometric mean      | (ref)                                                      | 1.01x faster                                                           |

Benchmark hidden because not significant (2): pickle_list, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                    | 13.3 ms: 1.14x faster                                                  |
| python_startup_no_site | 12.3 ms                                                    | 11.6 ms: 1.06x faster                                                  |
| Geometric mean         | (ref)                                                      | 1.10x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 6.99 ms                                                    | 6.93 ms: 1.01x faster                                                  |
| genshi_xml     | 29.9 ms                                                    | 31.5 ms: 1.05x slower                                                  |
| genshi_text    | 13.9 ms                                                    | 14.7 ms: 1.06x slower                                                  |
| Geometric mean | (ref)                                                      | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240408-darwin-arm64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------------|:----------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols         | 87.6 us                                                    | 70.4 us: 1.24x faster                                                  |
| tomli_loads                      | 1.47 sec                                                   | 1.28 sec: 1.15x faster                                                 |
| python_startup                   | 15.2 ms                                                    | 13.3 ms: 1.14x faster                                                  |
| pylint                           | 170 ms                                                     | 152 ms: 1.12x faster                                                   |
| richards                         | 31.8 ms                                                    | 29.3 ms: 1.09x faster                                                  |
| xml_etree_parse                  | 106 ms                                                     | 98.5 ms: 1.07x faster                                                  |
| richards_super                   | 35.2 ms                                                    | 32.8 ms: 1.07x faster                                                  |
| crypto_pyaes                     | 49.5 ms                                                    | 46.4 ms: 1.07x faster                                                  |
| python_startup_no_site           | 12.3 ms                                                    | 11.6 ms: 1.06x faster                                                  |
| xml_etree_iterparse              | 71.5 ms                                                    | 68.5 ms: 1.04x faster                                                  |
| async_tree_none                  | 209 ms                                                     | 202 ms: 1.03x faster                                                   |
| pickle                           | 7.48 us                                                    | 7.25 us: 1.03x faster                                                  |
| bench_mp_pool                    | 47.2 ms                                                    | 46.1 ms: 1.02x faster                                                  |
| pyflate                          | 321 ms                                                     | 315 ms: 1.02x faster                                                   |
| pickle_dict                      | 18.3 us                                                    | 18.1 us: 1.01x faster                                                  |
| regex_v8                         | 17.3 ms                                                    | 17.1 ms: 1.01x faster                                                  |
| mako                             | 6.99 ms                                                    | 6.93 ms: 1.01x faster                                                  |
| asyncio_websockets               | 409 ms                                                     | 408 ms: 1.00x faster                                                   |
| pidigits                         | 282 ms                                                     | 282 ms: 1.00x slower                                                   |
| json_loads                       | 16.8 us                                                    | 16.9 us: 1.00x slower                                                  |
| xml_etree_process                | 37.1 ms                                                    | 37.3 ms: 1.01x slower                                                  |
| json                             | 2.93 ms                                                    | 2.96 ms: 1.01x slower                                                  |
| float                            | 48.6 ms                                                    | 49.2 ms: 1.01x slower                                                  |
| async_tree_eager_cpu_io_mixed_tg | 331 ms                                                     | 335 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl                  | 1.29 sec                                                   | 1.31 sec: 1.01x slower                                                 |
| json_dumps                       | 6.23 ms                                                    | 6.32 ms: 1.01x slower                                                  |
| unpickle                         | 9.12 us                                                    | 9.27 us: 1.02x slower                                                  |
| pickle_pure_python               | 179 us                                                     | 182 us: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 358 ms                                                     | 365 ms: 1.02x slower                                                   |
| regex_effbot                     | 2.58 ms                                                    | 2.64 ms: 1.02x slower                                                  |
| regex_dna                        | 149 ms                                                     | 152 ms: 1.02x slower                                                   |
| sqlite_synth                     | 1.55 us                                                    | 1.58 us: 1.02x slower                                                  |
| scimark_monte_carlo              | 42.5 ms                                                    | 43.4 ms: 1.02x slower                                                  |
| deepcopy_reduce                  | 1.82 us                                                    | 1.86 us: 1.02x slower                                                  |
| thrift                           | 435 us                                                     | 447 us: 1.03x slower                                                   |
| deepcopy                         | 204 us                                                     | 209 us: 1.03x slower                                                   |
| mdp                              | 1.53 sec                                                   | 1.58 sec: 1.03x slower                                                 |
| coverage                         | 45.0 ms                                                    | 46.4 ms: 1.03x slower                                                  |
| xml_etree_generate               | 52.7 ms                                                    | 54.4 ms: 1.03x slower                                                  |
| pycparser                        | 632 ms                                                     | 653 ms: 1.03x slower                                                   |
| logging_format                   | 3.31 us                                                    | 3.42 us: 1.03x slower                                                  |
| logging_simple                   | 3.04 us                                                    | 3.14 us: 1.03x slower                                                  |
| unpickle_list                    | 2.88 us                                                    | 2.99 us: 1.04x slower                                                  |
| pprint_pformat                   | 947 ms                                                     | 987 ms: 1.04x slower                                                   |
| chameleon                        | 4.27 ms                                                    | 4.46 ms: 1.04x slower                                                  |
| dulwich_log                      | 27.6 ms                                                    | 28.8 ms: 1.05x slower                                                  |
| async_tree_eager_memoization_tg  | 126 ms                                                     | 131 ms: 1.05x slower                                                   |
| async_tree_eager_tg              | 41.4 ms                                                    | 43.3 ms: 1.05x slower                                                  |
| fannkuch                         | 248 ms                                                     | 260 ms: 1.05x slower                                                   |
| pprint_safe_repr                 | 465 ms                                                     | 488 ms: 1.05x slower                                                   |
| sympy_expand                     | 226 ms                                                     | 237 ms: 1.05x slower                                                   |
| sqlglot_parse                    | 732 us                                                     | 770 us: 1.05x slower                                                   |
| genshi_xml                       | 29.9 ms                                                    | 31.5 ms: 1.05x slower                                                  |
| html5lib                         | 31.2 ms                                                    | 32.8 ms: 1.05x slower                                                  |
| meteor_contest                   | 70.3 ms                                                    | 74.0 ms: 1.05x slower                                                  |
| logging_silent                   | 60.1 ns                                                    | 63.6 ns: 1.06x slower                                                  |
| sqlglot_normalize                | 166 ms                                                     | 175 ms: 1.06x slower                                                   |
| go                               | 101 ms                                                     | 106 ms: 1.06x slower                                                   |
| sqlglot_transpile                | 891 us                                                     | 943 us: 1.06x slower                                                   |
| genshi_text                      | 13.9 ms                                                    | 14.7 ms: 1.06x slower                                                  |
| coroutines                       | 15.8 ms                                                    | 16.8 ms: 1.06x slower                                                  |
| async_generators                 | 281 ms                                                     | 299 ms: 1.06x slower                                                   |
| 2to3                             | 161 ms                                                     | 171 ms: 1.07x slower                                                   |
| pathlib                          | 23.3 ms                                                    | 24.9 ms: 1.07x slower                                                  |
| deepcopy_memo                    | 22.6 us                                                    | 24.1 us: 1.07x slower                                                  |
| mypy2                            | 379 ms                                                     | 406 ms: 1.07x slower                                                   |
| sympy_str                        | 131 ms                                                     | 142 ms: 1.08x slower                                                   |
| async_tree_eager                 | 60.3 ms                                                    | 65.1 ms: 1.08x slower                                                  |
| docutils                         | 1.44 sec                                                   | 1.55 sec: 1.08x slower                                                 |
| sqlglot_optimize                 | 30.9 ms                                                    | 33.6 ms: 1.09x slower                                                  |
| async_tree_memoization_tg        | 240 ms                                                     | 260 ms: 1.09x slower                                                   |
| bench_thread_pool                | 447 us                                                     | 487 us: 1.09x slower                                                   |
| sympy_integrate                  | 10.3 ms                                                    | 11.4 ms: 1.10x slower                                                  |
| sympy_sum                        | 69.2 ms                                                    | 76.4 ms: 1.10x slower                                                  |
| raytrace                         | 147 ms                                                     | 163 ms: 1.11x slower                                                   |
| scimark_fft                      | 181 ms                                                     | 200 ms: 1.11x slower                                                   |
| chaos                            | 34.0 ms                                                    | 38.0 ms: 1.12x slower                                                  |
| spectral_norm                    | 66.4 ms                                                    | 74.3 ms: 1.12x slower                                                  |
| aiohttp                          | 997 us                                                     | 1.12 ms: 1.12x slower                                                  |
| scimark_sor                      | 94.9 ms                                                    | 106 ms: 1.12x slower                                                   |
| scimark_sparse_mat_mult          | 2.77 ms                                                    | 3.14 ms: 1.13x slower                                                  |
| generators                       | 22.9 ms                                                    | 26.0 ms: 1.14x slower                                                  |
| deltablue                        | 2.14 ms                                                    | 2.47 ms: 1.15x slower                                                  |
| nqueens                          | 52.2 ms                                                    | 60.3 ms: 1.15x slower                                                  |
| gunicorn                         | 1.04 ms                                                    | 1.20 ms: 1.16x slower                                                  |
| comprehensions                   | 10.2 us                                                    | 12.0 us: 1.18x slower                                                  |
| hexiom                           | 4.06 ms                                                    | 4.81 ms: 1.18x slower                                                  |
| nbody                            | 59.6 ms                                                    | 70.6 ms: 1.18x slower                                                  |
| scimark_lu                       | 66.9 ms                                                    | 82.0 ms: 1.23x slower                                                  |
| tornado_http                     | 66.7 ms                                                    | 82.6 ms: 1.24x slower                                                  |
| regex_compile                    | 68.5 ms                                                    | 85.3 ms: 1.24x slower                                                  |
| Geometric mean                   | (ref)                                                      | 1.04x slower                                                           |

Benchmark hidden because not significant (16): async_tree_eager_io_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_none_tg, pickle_list, gc_traversal, unpickle_pure_python, dask, telco, create_gc_cycles, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_eager_io, async_tree_memoization, async_tree_eager_memoization, asyncio_tcp
Ignored benchmarks (3) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-darwin-arm64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, django_template, flaskblogging

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.17x