# Results vs. 3.10.4

- fork: mdboom
- ref: tier2_func_simple
- machine: darwin-arm64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 172 ms: 1.12x faster                                                |
| chameleon      | 6.26 ms                                                | 4.50 ms: 1.39x faster                                               |
| docutils       | 1.73 sec                                               | 1.56 sec: 1.11x faster                                              |
| html5lib       | 42.4 ms                                                | 33.2 ms: 1.27x faster                                               |
| Geometric mean | (ref)                                                  | 1.19x faster                                                        |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 204 ms: 1.90x faster                                                |
| async_tree_memoization  | 474 ms                                                 | 263 ms: 1.80x faster                                                |
| async_tree_io           | 980 ms                                                 | 569 ms: 1.72x faster                                                |
| async_tree_cpu_io_mixed | 649 ms                                                 | 464 ms: 1.40x faster                                                |
| Geometric mean          | (ref)                                                  | 1.70x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 69.0 ms                                                | 48.9 ms: 1.41x faster                                               |
| nbody          | 93.0 ms                                                | 70.7 ms: 1.32x faster                                               |
| Geometric mean | (ref)                                                  | 1.23x faster                                                        |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 174 ms                                                 | 153 ms: 1.14x faster                                                |
| regex_compile  | 95.3 ms                                                | 84.6 ms: 1.13x faster                                               |
| regex_v8       | 17.1 ms                                                | 17.2 ms: 1.01x slower                                               |
| regex_effbot   | 2.46 ms                                                | 2.73 ms: 1.11x slower                                               |
| Geometric mean | (ref)                                                  | 1.04x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 182 us: 1.55x faster                                                |
| unpickle_pure_python | 194 us                                                 | 141 us: 1.37x faster                                                |
| tomli_loads          | 1.71 sec                                               | 1.28 sec: 1.33x faster                                              |
| json_dumps           | 8.11 ms                                                | 6.38 ms: 1.27x faster                                               |
| xml_etree_process    | 46.5 ms                                                | 37.3 ms: 1.25x faster                                               |
| xml_etree_parse      | 108 ms                                                 | 106 ms: 1.02x faster                                                |
| xml_etree_iterparse  | 72.1 ms                                                | 72.6 ms: 1.01x slower                                               |
| xml_etree_generate   | 53.5 ms                                                | 54.6 ms: 1.02x slower                                               |
| json_loads           | 16.4 us                                                | 16.9 us: 1.03x slower                                               |
| pickle               | 6.97 us                                                | 7.44 us: 1.07x slower                                               |
| pickle_dict          | 17.0 us                                                | 18.1 us: 1.07x slower                                               |
| pickle_list          | 2.74 us                                                | 2.96 us: 1.08x slower                                               |
| unpickle             | 8.80 us                                                | 9.62 us: 1.09x slower                                               |
| unpickle_list        | 2.69 us                                                | 3.04 us: 1.13x slower                                               |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 13.5 ms: 1.24x slower                                               |
| python_startup_no_site | 7.91 ms                                                | 11.7 ms: 1.47x slower                                               |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako           | 9.87 ms                                                | 6.95 ms: 1.42x faster                                               |
| genshi_text    | 17.3 ms                                                | 14.8 ms: 1.17x faster                                               |
| genshi_xml     | 33.8 ms                                                | 31.1 ms: 1.09x faster                                               |
| Geometric mean | (ref)                                                  | 1.22x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 69.7 us: 4.63x faster                                               |
| deltablue                | 4.91 ms                                                | 2.47 ms: 1.99x faster                                               |
| async_tree_none          | 388 ms                                                 | 204 ms: 1.90x faster                                                |
| raytrace                 | 301 ms                                                 | 163 ms: 1.85x faster                                                |
| async_tree_memoization   | 474 ms                                                 | 263 ms: 1.80x faster                                                |
| logging_silent           | 117 ns                                                 | 65.4 ns: 1.79x faster                                               |
| pylint                   | 277 ms                                                 | 155 ms: 1.79x faster                                                |
| richards_super           | 57.8 ms                                                | 33.0 ms: 1.75x faster                                               |
| chaos                    | 65.8 ms                                                | 38.0 ms: 1.73x faster                                               |
| async_tree_io            | 980 ms                                                 | 569 ms: 1.72x faster                                                |
| richards                 | 48.7 ms                                                | 29.7 ms: 1.64x faster                                               |
| sqlglot_parse            | 1.24 ms                                                | 761 us: 1.63x faster                                                |
| asyncio_tcp              | 659 ms                                                 | 405 ms: 1.63x faster                                                |
| sqlglot_transpile        | 1.44 ms                                                | 931 us: 1.55x faster                                                |
| pickle_pure_python       | 281 us                                                 | 182 us: 1.55x faster                                                |
| crypto_pyaes             | 71.8 ms                                                | 46.6 ms: 1.54x faster                                               |
| scimark_monte_carlo      | 65.6 ms                                                | 43.7 ms: 1.50x faster                                               |
| mypy2                    | 607 ms                                                 | 410 ms: 1.48x faster                                                |
| deepcopy_memo            | 34.7 us                                                | 24.2 us: 1.43x faster                                               |
| mako                     | 9.87 ms                                                | 6.95 ms: 1.42x faster                                               |
| go                       | 151 ms                                                 | 106 ms: 1.42x faster                                                |
| float                    | 69.0 ms                                                | 48.9 ms: 1.41x faster                                               |
| logging_format           | 4.83 us                                                | 3.44 us: 1.41x faster                                               |
| logging_simple           | 4.45 us                                                | 3.17 us: 1.40x faster                                               |
| comprehensions           | 16.9 us                                                | 12.1 us: 1.40x faster                                               |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 464 ms: 1.40x faster                                                |
| chameleon                | 6.26 ms                                                | 4.50 ms: 1.39x faster                                               |
| unpickle_pure_python     | 194 us                                                 | 141 us: 1.37x faster                                                |
| pyflate                  | 427 ms                                                 | 318 ms: 1.34x faster                                                |
| pycparser                | 877 ms                                                 | 654 ms: 1.34x faster                                                |
| tomli_loads              | 1.71 sec                                               | 1.28 sec: 1.33x faster                                              |
| pprint_pformat           | 1.30 sec                                               | 986 ms: 1.32x faster                                                |
| nbody                    | 93.0 ms                                                | 70.7 ms: 1.32x faster                                               |
| pprint_safe_repr         | 641 ms                                                 | 488 ms: 1.31x faster                                                |
| hexiom                   | 6.19 ms                                                | 4.82 ms: 1.29x faster                                               |
| deepcopy                 | 272 us                                                 | 212 us: 1.28x faster                                                |
| thrift                   | 572 us                                                 | 447 us: 1.28x faster                                                |
| html5lib                 | 42.4 ms                                                | 33.2 ms: 1.27x faster                                               |
| json_dumps               | 8.11 ms                                                | 6.38 ms: 1.27x faster                                               |
| spectral_norm            | 94.8 ms                                                | 75.1 ms: 1.26x faster                                               |
| deepcopy_reduce          | 2.33 us                                                | 1.86 us: 1.25x faster                                               |
| scimark_lu               | 103 ms                                                 | 82.4 ms: 1.25x faster                                               |
| xml_etree_process        | 46.5 ms                                                | 37.3 ms: 1.25x faster                                               |
| generators               | 32.3 ms                                                | 26.2 ms: 1.24x faster                                               |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.30 sec: 1.23x faster                                              |
| dulwich_log              | 35.3 ms                                                | 28.9 ms: 1.22x faster                                               |
| coroutines               | 20.7 ms                                                | 17.0 ms: 1.22x faster                                               |
| scimark_sor              | 128 ms                                                 | 106 ms: 1.20x faster                                                |
| sympy_sum                | 92.2 ms                                                | 76.8 ms: 1.20x faster                                               |
| genshi_text              | 17.3 ms                                                | 14.8 ms: 1.17x faster                                               |
| sympy_str                | 165 ms                                                 | 143 ms: 1.16x faster                                                |
| fannkuch                 | 303 ms                                                 | 262 ms: 1.16x faster                                                |
| dask                     | 253 ms                                                 | 220 ms: 1.15x faster                                                |
| sympy_integrate          | 13.1 ms                                                | 11.4 ms: 1.15x faster                                               |
| regex_dna                | 174 ms                                                 | 153 ms: 1.14x faster                                                |
| sympy_expand             | 269 ms                                                 | 238 ms: 1.13x faster                                                |
| regex_compile            | 95.3 ms                                                | 84.6 ms: 1.13x faster                                               |
| 2to3                     | 192 ms                                                 | 172 ms: 1.12x faster                                                |
| docutils                 | 1.73 sec                                               | 1.56 sec: 1.11x faster                                              |
| scimark_fft              | 224 ms                                                 | 203 ms: 1.11x faster                                                |
| aiohttp                  | 1.22 ms                                                | 1.12 ms: 1.09x faster                                               |
| sqlglot_optimize         | 36.8 ms                                                | 33.7 ms: 1.09x faster                                               |
| genshi_xml               | 33.8 ms                                                | 31.1 ms: 1.09x faster                                               |
| sqlglot_normalize        | 190 ms                                                 | 176 ms: 1.08x faster                                                |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.18 ms: 1.08x faster                                               |
| bench_thread_pool        | 527 us                                                 | 490 us: 1.08x faster                                                |
| gunicorn                 | 1.30 ms                                                | 1.22 ms: 1.07x faster                                               |
| nqueens                  | 63.8 ms                                                | 60.6 ms: 1.05x faster                                               |
| meteor_contest           | 77.7 ms                                                | 74.0 ms: 1.05x faster                                               |
| mdp                      | 1.63 sec                                               | 1.58 sec: 1.03x faster                                              |
| xml_etree_parse          | 108 ms                                                 | 106 ms: 1.02x faster                                                |
| json                     | 3.08 ms                                                | 3.03 ms: 1.02x faster                                               |
| regex_v8                 | 17.1 ms                                                | 17.2 ms: 1.01x slower                                               |
| xml_etree_iterparse      | 72.1 ms                                                | 72.6 ms: 1.01x slower                                               |
| xml_etree_generate       | 53.5 ms                                                | 54.6 ms: 1.02x slower                                               |
| pathlib                  | 24.5 ms                                                | 25.2 ms: 1.03x slower                                               |
| json_loads               | 16.4 us                                                | 16.9 us: 1.03x slower                                               |
| gc_traversal             | 2.36 ms                                                | 2.46 ms: 1.04x slower                                               |
| create_gc_cycles         | 860 us                                                 | 900 us: 1.05x slower                                                |
| pickle                   | 6.97 us                                                | 7.44 us: 1.07x slower                                               |
| pickle_dict              | 17.0 us                                                | 18.1 us: 1.07x slower                                               |
| pickle_list              | 2.74 us                                                | 2.96 us: 1.08x slower                                               |
| sqlite_synth             | 1.46 us                                                | 1.59 us: 1.09x slower                                               |
| unpickle                 | 8.80 us                                                | 9.62 us: 1.09x slower                                               |
| regex_effbot             | 2.46 ms                                                | 2.73 ms: 1.11x slower                                               |
| coverage                 | 41.5 ms                                                | 46.6 ms: 1.12x slower                                               |
| unpickle_list            | 2.69 us                                                | 3.04 us: 1.13x slower                                               |
| bench_mp_pool            | 37.4 ms                                                | 46.1 ms: 1.23x slower                                               |
| python_startup           | 10.9 ms                                                | 13.5 ms: 1.24x slower                                               |
| async_generators         | 231 ms                                                 | 300 ms: 1.30x slower                                                |
| telco                    | 3.49 ms                                                | 4.75 ms: 1.36x slower                                               |
| python_startup_no_site   | 7.91 ms                                                | 11.7 ms: 1.47x slower                                               |
| Geometric mean           | (ref)                                                  | 1.22x faster                                                        |

Benchmark hidden because not significant (3): tornado_http, asyncio_websockets, pidigits
Ignored benchmarks (5) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240405-3.13.0a5+-81bda60-JIT/bm-20240405-darwin-arm64-mdboom-tier2_func_simple-3.13.0a5+-81bda60.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: 1.39x