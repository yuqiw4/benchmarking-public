# Results vs. 3.10.4

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: darwin-arm64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.25x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 162 ms: 1.18x faster                                                             |
| chameleon      | 6.26 ms                                                | 4.40 ms: 1.42x faster                                                            |
| docutils       | 1.73 sec                                               | 1.49 sec: 1.16x faster                                                           |
| html5lib       | 42.4 ms                                                | 33.6 ms: 1.26x faster                                                            |
| tornado_http   | 86.7 ms                                                | 75.6 ms: 1.15x faster                                                            |
| Geometric mean | (ref)                                                  | 1.23x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 202 ms: 1.92x faster                                                             |
| async_tree_memoization  | 474 ms                                                 | 260 ms: 1.82x faster                                                             |
| async_tree_io           | 980 ms                                                 | 567 ms: 1.73x faster                                                             |
| async_tree_cpu_io_mixed | 649 ms                                                 | 462 ms: 1.41x faster                                                             |
| Geometric mean          | (ref)                                                  | 1.71x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 93.0 ms                                                | 65.0 ms: 1.43x faster                                                            |
| float          | 69.0 ms                                                | 51.0 ms: 1.35x faster                                                            |
| Geometric mean | (ref)                                                  | 1.25x faster                                                                     |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 95.3 ms                                                | 70.2 ms: 1.36x faster                                                            |
| regex_dna      | 174 ms                                                 | 155 ms: 1.13x faster                                                             |
| regex_v8       | 17.1 ms                                                | 17.4 ms: 1.02x slower                                                            |
| regex_effbot   | 2.46 ms                                                | 2.72 ms: 1.11x slower                                                            |
| Geometric mean | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 183 us: 1.53x faster                                                             |
| unpickle_pure_python | 194 us                                                 | 146 us: 1.33x faster                                                             |
| json_dumps           | 8.11 ms                                                | 6.25 ms: 1.30x faster                                                            |
| xml_etree_process    | 46.5 ms                                                | 37.4 ms: 1.24x faster                                                            |
| tomli_loads          | 1.71 sec                                               | 1.50 sec: 1.13x faster                                                           |
| xml_etree_parse      | 108 ms                                                 | 99.6 ms: 1.08x faster                                                            |
| xml_etree_iterparse  | 72.1 ms                                                | 68.8 ms: 1.05x faster                                                            |
| xml_etree_generate   | 53.5 ms                                                | 54.2 ms: 1.01x slower                                                            |
| json_loads           | 16.4 us                                                | 17.0 us: 1.03x slower                                                            |
| unpickle             | 8.80 us                                                | 9.30 us: 1.06x slower                                                            |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.07x slower                                                            |
| pickle               | 6.97 us                                                | 7.48 us: 1.07x slower                                                            |
| pickle_list          | 2.74 us                                                | 2.95 us: 1.08x slower                                                            |
| unpickle_list        | 2.69 us                                                | 3.02 us: 1.12x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 12.0 ms: 1.10x slower                                                            |
| python_startup_no_site | 7.91 ms                                                | 10.3 ms: 1.30x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 9.87 ms                                                | 7.14 ms: 1.38x faster                                                            |
| genshi_text    | 17.3 ms                                                | 14.6 ms: 1.19x faster                                                            |
| genshi_xml     | 33.8 ms                                                | 31.6 ms: 1.07x faster                                                            |
| Geometric mean | (ref)                                                  | 1.21x faster                                                                     |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 69.4 us: 4.66x faster                                                            |
| deltablue                | 4.91 ms                                                | 2.20 ms: 2.24x faster                                                            |
| raytrace                 | 301 ms                                                 | 153 ms: 1.97x faster                                                             |
| pylint                   | 277 ms                                                 | 144 ms: 1.92x faster                                                             |
| async_tree_none          | 388 ms                                                 | 202 ms: 1.92x faster                                                             |
| chaos                    | 65.8 ms                                                | 35.9 ms: 1.83x faster                                                            |
| logging_silent           | 117 ns                                                 | 64.3 ns: 1.82x faster                                                            |
| async_tree_memoization   | 474 ms                                                 | 260 ms: 1.82x faster                                                             |
| async_tree_io            | 980 ms                                                 | 567 ms: 1.73x faster                                                             |
| richards_super           | 57.8 ms                                                | 34.5 ms: 1.68x faster                                                            |
| sqlglot_parse            | 1.24 ms                                                | 747 us: 1.66x faster                                                             |
| comprehensions           | 16.9 us                                                | 10.2 us: 1.66x faster                                                            |
| mypy2                    | 607 ms                                                 | 382 ms: 1.59x faster                                                             |
| sqlglot_transpile        | 1.44 ms                                                | 907 us: 1.59x faster                                                             |
| richards                 | 48.7 ms                                                | 30.6 ms: 1.59x faster                                                            |
| asyncio_tcp              | 659 ms                                                 | 416 ms: 1.58x faster                                                             |
| crypto_pyaes             | 71.8 ms                                                | 46.3 ms: 1.55x faster                                                            |
| pickle_pure_python       | 281 us                                                 | 183 us: 1.53x faster                                                             |
| scimark_lu               | 103 ms                                                 | 68.5 ms: 1.50x faster                                                            |
| go                       | 151 ms                                                 | 101 ms: 1.50x faster                                                             |
| scimark_monte_carlo      | 65.6 ms                                                | 44.1 ms: 1.49x faster                                                            |
| hexiom                   | 6.19 ms                                                | 4.20 ms: 1.47x faster                                                            |
| deepcopy_memo            | 34.7 us                                                | 23.7 us: 1.47x faster                                                            |
| nbody                    | 93.0 ms                                                | 65.0 ms: 1.43x faster                                                            |
| chameleon                | 6.26 ms                                                | 4.40 ms: 1.42x faster                                                            |
| logging_format           | 4.83 us                                                | 3.42 us: 1.41x faster                                                            |
| logging_simple           | 4.45 us                                                | 3.16 us: 1.41x faster                                                            |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 462 ms: 1.41x faster                                                             |
| mako                     | 9.87 ms                                                | 7.14 ms: 1.38x faster                                                            |
| pycparser                | 877 ms                                                 | 644 ms: 1.36x faster                                                             |
| regex_compile            | 95.3 ms                                                | 70.2 ms: 1.36x faster                                                            |
| float                    | 69.0 ms                                                | 51.0 ms: 1.35x faster                                                            |
| unpickle_pure_python     | 194 us                                                 | 146 us: 1.33x faster                                                             |
| spectral_norm            | 94.8 ms                                                | 71.2 ms: 1.33x faster                                                            |
| pprint_pformat           | 1.30 sec                                               | 983 ms: 1.33x faster                                                             |
| pprint_safe_repr         | 641 ms                                                 | 483 ms: 1.32x faster                                                             |
| pyflate                  | 427 ms                                                 | 325 ms: 1.31x faster                                                             |
| sympy_sum                | 92.2 ms                                                | 71.0 ms: 1.30x faster                                                            |
| json_dumps               | 8.11 ms                                                | 6.25 ms: 1.30x faster                                                            |
| deepcopy                 | 272 us                                                 | 209 us: 1.30x faster                                                             |
| thrift                   | 572 us                                                 | 442 us: 1.29x faster                                                             |
| scimark_sor              | 128 ms                                                 | 99.2 ms: 1.29x faster                                                            |
| html5lib                 | 42.4 ms                                                | 33.6 ms: 1.26x faster                                                            |
| sympy_integrate          | 13.1 ms                                                | 10.5 ms: 1.26x faster                                                            |
| dulwich_log              | 35.3 ms                                                | 28.2 ms: 1.25x faster                                                            |
| xml_etree_process        | 46.5 ms                                                | 37.4 ms: 1.24x faster                                                            |
| deepcopy_reduce          | 2.33 us                                                | 1.88 us: 1.24x faster                                                            |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.31 sec: 1.23x faster                                                           |
| sympy_str                | 165 ms                                                 | 135 ms: 1.22x faster                                                             |
| coroutines               | 20.7 ms                                                | 17.0 ms: 1.22x faster                                                            |
| genshi_text              | 17.3 ms                                                | 14.6 ms: 1.19x faster                                                            |
| generators               | 32.3 ms                                                | 27.4 ms: 1.18x faster                                                            |
| 2to3                     | 192 ms                                                 | 162 ms: 1.18x faster                                                             |
| sympy_expand             | 269 ms                                                 | 230 ms: 1.17x faster                                                             |
| fannkuch                 | 303 ms                                                 | 260 ms: 1.16x faster                                                             |
| docutils                 | 1.73 sec                                               | 1.49 sec: 1.16x faster                                                           |
| dask                     | 253 ms                                                 | 219 ms: 1.16x faster                                                             |
| sqlglot_optimize         | 36.8 ms                                                | 31.9 ms: 1.15x faster                                                            |
| scimark_fft              | 224 ms                                                 | 195 ms: 1.15x faster                                                             |
| tornado_http             | 86.7 ms                                                | 75.6 ms: 1.15x faster                                                            |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.00 ms: 1.14x faster                                                            |
| nqueens                  | 63.8 ms                                                | 56.0 ms: 1.14x faster                                                            |
| tomli_loads              | 1.71 sec                                               | 1.50 sec: 1.13x faster                                                           |
| regex_dna                | 174 ms                                                 | 155 ms: 1.13x faster                                                             |
| gunicorn                 | 1.30 ms                                                | 1.16 ms: 1.12x faster                                                            |
| bench_thread_pool        | 527 us                                                 | 471 us: 1.12x faster                                                             |
| sqlglot_normalize        | 190 ms                                                 | 171 ms: 1.11x faster                                                             |
| aiohttp                  | 1.22 ms                                                | 1.10 ms: 1.11x faster                                                            |
| meteor_contest           | 77.7 ms                                                | 71.7 ms: 1.08x faster                                                            |
| xml_etree_parse          | 108 ms                                                 | 99.6 ms: 1.08x faster                                                            |
| genshi_xml               | 33.8 ms                                                | 31.6 ms: 1.07x faster                                                            |
| mdp                      | 1.63 sec                                               | 1.53 sec: 1.06x faster                                                           |
| xml_etree_iterparse      | 72.1 ms                                                | 68.8 ms: 1.05x faster                                                            |
| json                     | 3.08 ms                                                | 2.95 ms: 1.04x faster                                                            |
| asyncio_websockets       | 410 ms                                                 | 408 ms: 1.00x faster                                                             |
| pathlib                  | 24.5 ms                                                | 24.8 ms: 1.01x slower                                                            |
| xml_etree_generate       | 53.5 ms                                                | 54.2 ms: 1.01x slower                                                            |
| regex_v8                 | 17.1 ms                                                | 17.4 ms: 1.02x slower                                                            |
| create_gc_cycles         | 860 us                                                 | 885 us: 1.03x slower                                                             |
| gc_traversal             | 2.36 ms                                                | 2.44 ms: 1.03x slower                                                            |
| json_loads               | 16.4 us                                                | 17.0 us: 1.03x slower                                                            |
| unpickle                 | 8.80 us                                                | 9.30 us: 1.06x slower                                                            |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.07x slower                                                            |
| sqlite_synth             | 1.46 us                                                | 1.56 us: 1.07x slower                                                            |
| pickle                   | 6.97 us                                                | 7.48 us: 1.07x slower                                                            |
| pickle_list              | 2.74 us                                                | 2.95 us: 1.08x slower                                                            |
| python_startup           | 10.9 ms                                                | 12.0 ms: 1.10x slower                                                            |
| regex_effbot             | 2.46 ms                                                | 2.72 ms: 1.11x slower                                                            |
| coverage                 | 41.5 ms                                                | 46.4 ms: 1.12x slower                                                            |
| unpickle_list            | 2.69 us                                                | 3.02 us: 1.12x slower                                                            |
| bench_mp_pool            | 37.4 ms                                                | 42.8 ms: 1.15x slower                                                            |
| async_generators         | 231 ms                                                 | 287 ms: 1.24x slower                                                             |
| python_startup_no_site   | 7.91 ms                                                | 10.3 ms: 1.30x slower                                                            |
| telco                    | 3.49 ms                                                | 4.65 ms: 1.33x slower                                                            |
| Geometric mean           | (ref)                                                  | 1.25x faster                                                                     |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240408-3.13.0a5+-4675ce8/bm-20240408-darwin-arm64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.14x