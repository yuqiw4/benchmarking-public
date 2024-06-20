# Results vs. 3.10.4

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: darwin-arm64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.25x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 161 ms: 1.19x faster                                                   |
| chameleon      | 6.26 ms                                                | 4.49 ms: 1.39x faster                                                  |
| docutils       | 1.73 sec                                               | 1.45 sec: 1.19x faster                                                 |
| html5lib       | 42.4 ms                                                | 31.9 ms: 1.33x faster                                                  |
| tornado_http   | 86.7 ms                                                | 75.0 ms: 1.16x faster                                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 202 ms: 1.92x faster                                                   |
| async_tree_memoization  | 474 ms                                                 | 270 ms: 1.75x faster                                                   |
| async_tree_io           | 980 ms                                                 | 566 ms: 1.73x faster                                                   |
| async_tree_cpu_io_mixed | 649 ms                                                 | 463 ms: 1.40x faster                                                   |
| Geometric mean          | (ref)                                                  | 1.69x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 93.0 ms                                                | 65.2 ms: 1.43x faster                                                  |
| float          | 69.0 ms                                                | 50.8 ms: 1.36x faster                                                  |
| Geometric mean | (ref)                                                  | 1.25x faster                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 95.3 ms                                                | 69.4 ms: 1.37x faster                                                  |
| regex_dna      | 174 ms                                                 | 149 ms: 1.17x faster                                                   |
| regex_v8       | 17.1 ms                                                | 17.4 ms: 1.01x slower                                                  |
| regex_effbot   | 2.46 ms                                                | 2.63 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 183 us: 1.54x faster                                                   |
| unpickle_pure_python | 194 us                                                 | 143 us: 1.36x faster                                                   |
| json_dumps           | 8.11 ms                                                | 6.26 ms: 1.29x faster                                                  |
| xml_etree_process    | 46.5 ms                                                | 37.9 ms: 1.23x faster                                                  |
| tomli_loads          | 1.71 sec                                               | 1.50 sec: 1.14x faster                                                 |
| xml_etree_parse      | 108 ms                                                 | 99.0 ms: 1.09x faster                                                  |
| xml_etree_iterparse  | 72.1 ms                                                | 68.8 ms: 1.05x faster                                                  |
| xml_etree_generate   | 53.5 ms                                                | 54.9 ms: 1.03x slower                                                  |
| json_loads           | 16.4 us                                                | 17.1 us: 1.04x slower                                                  |
| unpickle             | 8.80 us                                                | 9.21 us: 1.05x slower                                                  |
| pickle               | 6.97 us                                                | 7.44 us: 1.07x slower                                                  |
| pickle_dict          | 17.0 us                                                | 18.2 us: 1.07x slower                                                  |
| unpickle_list        | 2.69 us                                                | 2.90 us: 1.08x slower                                                  |
| pickle_list          | 2.74 us                                                | 3.01 us: 1.10x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.08x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 11.9 ms: 1.09x slower                                                  |
| python_startup_no_site | 7.91 ms                                                | 9.12 ms: 1.15x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 9.87 ms                                                | 7.14 ms: 1.38x faster                                                  |
| django_template | 26.4 ms                                                | 20.1 ms: 1.31x faster                                                  |
| genshi_text     | 17.3 ms                                                | 14.7 ms: 1.18x faster                                                  |
| genshi_xml      | 33.8 ms                                                | 31.7 ms: 1.07x faster                                                  |
| Geometric mean  | (ref)                                                  | 1.23x faster                                                           |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 68.0 us: 4.75x faster                                                  |
| deltablue                | 4.91 ms                                                | 2.18 ms: 2.26x faster                                                  |
| raytrace                 | 301 ms                                                 | 153 ms: 1.97x faster                                                   |
| async_tree_none          | 388 ms                                                 | 202 ms: 1.92x faster                                                   |
| chaos                    | 65.8 ms                                                | 36.3 ms: 1.81x faster                                                  |
| logging_silent           | 117 ns                                                 | 64.8 ns: 1.81x faster                                                  |
| async_tree_memoization   | 474 ms                                                 | 270 ms: 1.75x faster                                                   |
| async_tree_io            | 980 ms                                                 | 566 ms: 1.73x faster                                                   |
| richards_super           | 57.8 ms                                                | 34.3 ms: 1.69x faster                                                  |
| sqlglot_parse            | 1.24 ms                                                | 749 us: 1.66x faster                                                   |
| pylint                   | 277 ms                                                 | 170 ms: 1.63x faster                                                   |
| asyncio_tcp              | 659 ms                                                 | 406 ms: 1.62x faster                                                   |
| comprehensions           | 16.9 us                                                | 10.6 us: 1.60x faster                                                  |
| mypy2                    | 607 ms                                                 | 380 ms: 1.60x faster                                                   |
| sqlglot_transpile        | 1.44 ms                                                | 908 us: 1.59x faster                                                   |
| richards                 | 48.7 ms                                                | 31.2 ms: 1.56x faster                                                  |
| crypto_pyaes             | 71.8 ms                                                | 46.5 ms: 1.54x faster                                                  |
| pickle_pure_python       | 281 us                                                 | 183 us: 1.54x faster                                                   |
| go                       | 151 ms                                                 | 100 ms: 1.50x faster                                                   |
| scimark_lu               | 103 ms                                                 | 68.9 ms: 1.49x faster                                                  |
| scimark_monte_carlo      | 65.6 ms                                                | 44.5 ms: 1.47x faster                                                  |
| hexiom                   | 6.19 ms                                                | 4.24 ms: 1.46x faster                                                  |
| deepcopy_memo            | 34.7 us                                                | 23.9 us: 1.45x faster                                                  |
| nbody                    | 93.0 ms                                                | 65.2 ms: 1.43x faster                                                  |
| logging_format           | 4.83 us                                                | 3.42 us: 1.41x faster                                                  |
| logging_simple           | 4.45 us                                                | 3.15 us: 1.41x faster                                                  |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 463 ms: 1.40x faster                                                   |
| chameleon                | 6.26 ms                                                | 4.49 ms: 1.39x faster                                                  |
| mako                     | 9.87 ms                                                | 7.14 ms: 1.38x faster                                                  |
| regex_compile            | 95.3 ms                                                | 69.4 ms: 1.37x faster                                                  |
| pycparser                | 877 ms                                                 | 640 ms: 1.37x faster                                                   |
| unpickle_pure_python     | 194 us                                                 | 143 us: 1.36x faster                                                   |
| float                    | 69.0 ms                                                | 50.8 ms: 1.36x faster                                                  |
| pprint_pformat           | 1.30 sec                                               | 972 ms: 1.34x faster                                                   |
| pprint_safe_repr         | 641 ms                                                 | 479 ms: 1.34x faster                                                   |
| spectral_norm            | 94.8 ms                                                | 71.0 ms: 1.34x faster                                                  |
| html5lib                 | 42.4 ms                                                | 31.9 ms: 1.33x faster                                                  |
| pyflate                  | 427 ms                                                 | 322 ms: 1.32x faster                                                   |
| django_template          | 26.4 ms                                                | 20.1 ms: 1.31x faster                                                  |
| sympy_sum                | 92.2 ms                                                | 70.6 ms: 1.31x faster                                                  |
| json_dumps               | 8.11 ms                                                | 6.26 ms: 1.29x faster                                                  |
| scimark_sor              | 128 ms                                                 | 99.4 ms: 1.29x faster                                                  |
| thrift                   | 572 us                                                 | 444 us: 1.29x faster                                                   |
| dulwich_log              | 35.3 ms                                                | 27.7 ms: 1.28x faster                                                  |
| sympy_integrate          | 13.1 ms                                                | 10.4 ms: 1.26x faster                                                  |
| deepcopy                 | 272 us                                                 | 216 us: 1.26x faster                                                   |
| sympy_str                | 165 ms                                                 | 134 ms: 1.24x faster                                                   |
| deepcopy_reduce          | 2.33 us                                                | 1.90 us: 1.23x faster                                                  |
| xml_etree_process        | 46.5 ms                                                | 37.9 ms: 1.23x faster                                                  |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.32 sec: 1.22x faster                                                 |
| coroutines               | 20.7 ms                                                | 17.2 ms: 1.20x faster                                                  |
| 2to3                     | 192 ms                                                 | 161 ms: 1.19x faster                                                   |
| docutils                 | 1.73 sec                                               | 1.45 sec: 1.19x faster                                                 |
| gunicorn                 | 1.30 ms                                                | 1.10 ms: 1.19x faster                                                  |
| genshi_text              | 17.3 ms                                                | 14.7 ms: 1.18x faster                                                  |
| sympy_expand             | 269 ms                                                 | 229 ms: 1.17x faster                                                   |
| fannkuch                 | 303 ms                                                 | 258 ms: 1.17x faster                                                   |
| regex_dna                | 174 ms                                                 | 149 ms: 1.17x faster                                                   |
| sqlglot_optimize         | 36.8 ms                                                | 31.5 ms: 1.17x faster                                                  |
| tornado_http             | 86.7 ms                                                | 75.0 ms: 1.16x faster                                                  |
| dask                     | 253 ms                                                 | 219 ms: 1.16x faster                                                   |
| scimark_fft              | 224 ms                                                 | 195 ms: 1.15x faster                                                   |
| aiohttp                  | 1.22 ms                                                | 1.07 ms: 1.14x faster                                                  |
| tomli_loads              | 1.71 sec                                               | 1.50 sec: 1.14x faster                                                 |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.02 ms: 1.14x faster                                                  |
| nqueens                  | 63.8 ms                                                | 56.3 ms: 1.13x faster                                                  |
| sqlglot_normalize        | 190 ms                                                 | 169 ms: 1.12x faster                                                   |
| generators               | 32.3 ms                                                | 28.9 ms: 1.12x faster                                                  |
| bench_thread_pool        | 527 us                                                 | 472 us: 1.12x faster                                                   |
| xml_etree_parse          | 108 ms                                                 | 99.0 ms: 1.09x faster                                                  |
| meteor_contest           | 77.7 ms                                                | 71.8 ms: 1.08x faster                                                  |
| genshi_xml               | 33.8 ms                                                | 31.7 ms: 1.07x faster                                                  |
| mdp                      | 1.63 sec                                               | 1.54 sec: 1.06x faster                                                 |
| xml_etree_iterparse      | 72.1 ms                                                | 68.8 ms: 1.05x faster                                                  |
| json                     | 3.08 ms                                                | 2.96 ms: 1.04x faster                                                  |
| pathlib                  | 24.5 ms                                                | 24.0 ms: 1.02x faster                                                  |
| asyncio_websockets       | 410 ms                                                 | 408 ms: 1.00x faster                                                   |
| regex_v8                 | 17.1 ms                                                | 17.4 ms: 1.01x slower                                                  |
| create_gc_cycles         | 860 us                                                 | 872 us: 1.01x slower                                                   |
| xml_etree_generate       | 53.5 ms                                                | 54.9 ms: 1.03x slower                                                  |
| gc_traversal             | 2.36 ms                                                | 2.44 ms: 1.03x slower                                                  |
| json_loads               | 16.4 us                                                | 17.1 us: 1.04x slower                                                  |
| unpickle                 | 8.80 us                                                | 9.21 us: 1.05x slower                                                  |
| pickle                   | 6.97 us                                                | 7.44 us: 1.07x slower                                                  |
| sqlite_synth             | 1.46 us                                                | 1.56 us: 1.07x slower                                                  |
| pickle_dict              | 17.0 us                                                | 18.2 us: 1.07x slower                                                  |
| regex_effbot             | 2.46 ms                                                | 2.63 ms: 1.07x slower                                                  |
| unpickle_list            | 2.69 us                                                | 2.90 us: 1.08x slower                                                  |
| python_startup           | 10.9 ms                                                | 11.9 ms: 1.09x slower                                                  |
| pickle_list              | 2.74 us                                                | 3.01 us: 1.10x slower                                                  |
| coverage                 | 41.5 ms                                                | 47.1 ms: 1.14x slower                                                  |
| python_startup_no_site   | 7.91 ms                                                | 9.12 ms: 1.15x slower                                                  |
| bench_mp_pool            | 37.4 ms                                                | 43.1 ms: 1.15x slower                                                  |
| async_generators         | 231 ms                                                 | 286 ms: 1.24x slower                                                   |
| telco                    | 3.49 ms                                                | 4.65 ms: 1.33x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.25x faster                                                           |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-darwin-arm64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: 1.15x