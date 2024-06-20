# Results vs. 3.10.4

- fork: savannahostrowski
- ref: llvm_18
- machine: darwin-arm64
- commit hash: b2bbeb0
- commit date: 2024-04-27
- overall geometric mean: 1.23x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 192 ms                                                 | 183 ms: 1.04x faster                                                 |
| chameleon      | 6.26 ms                                                | 4.45 ms: 1.41x faster                                                |
| docutils       | 1.73 sec                                               | 1.50 sec: 1.16x faster                                               |
| html5lib       | 42.4 ms                                                | 30.7 ms: 1.38x faster                                                |
| tornado_http   | 86.7 ms                                                | 71.5 ms: 1.21x faster                                                |
| Geometric mean | (ref)                                                  | 1.23x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none         | 388 ms                                                 | 198 ms: 1.96x faster                                                 |
| async_tree_memoization  | 474 ms                                                 | 268 ms: 1.77x faster                                                 |
| async_tree_io           | 980 ms                                                 | 558 ms: 1.76x faster                                                 |
| async_tree_cpu_io_mixed | 649 ms                                                 | 457 ms: 1.42x faster                                                 |
| Geometric mean          | (ref)                                                  | 1.72x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 93.0 ms                                                | 67.9 ms: 1.37x faster                                                |
| float          | 69.0 ms                                                | 50.7 ms: 1.36x faster                                                |
| Geometric mean | (ref)                                                  | 1.23x faster                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 95.3 ms                                                | 72.1 ms: 1.32x faster                                                |
| regex_dna      | 174 ms                                                 | 149 ms: 1.17x faster                                                 |
| regex_v8       | 17.1 ms                                                | 17.4 ms: 1.01x slower                                                |
| regex_effbot   | 2.46 ms                                                | 2.58 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                  | 1.10x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 281 us                                                 | 182 us: 1.54x faster                                                 |
| unpickle_pure_python | 194 us                                                 | 132 us: 1.48x faster                                                 |
| tomli_loads          | 1.71 sec                                               | 1.23 sec: 1.38x faster                                               |
| json_dumps           | 8.11 ms                                                | 6.31 ms: 1.28x faster                                                |
| xml_etree_process    | 46.5 ms                                                | 36.5 ms: 1.28x faster                                                |
| xml_etree_parse      | 108 ms                                                 | 104 ms: 1.04x faster                                                 |
| xml_etree_iterparse  | 72.1 ms                                                | 70.7 ms: 1.02x faster                                                |
| xml_etree_generate   | 53.5 ms                                                | 53.6 ms: 1.00x slower                                                |
| json_loads           | 16.4 us                                                | 17.0 us: 1.04x slower                                                |
| unpickle             | 8.80 us                                                | 9.29 us: 1.06x slower                                                |
| pickle_dict          | 17.0 us                                                | 18.2 us: 1.07x slower                                                |
| pickle               | 6.97 us                                                | 7.48 us: 1.07x slower                                                |
| unpickle_list        | 2.69 us                                                | 2.91 us: 1.08x slower                                                |
| pickle_list          | 2.74 us                                                | 2.98 us: 1.09x slower                                                |
| Geometric mean       | (ref)                                                  | 1.10x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 10.9 ms                                                | 14.1 ms: 1.30x slower                                                |
| python_startup_no_site | 7.91 ms                                                | 11.1 ms: 1.41x slower                                                |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 9.87 ms                                                | 6.40 ms: 1.54x faster                                                |
| django_template | 26.4 ms                                                | 20.8 ms: 1.27x faster                                                |
| genshi_text     | 17.3 ms                                                | 15.6 ms: 1.11x faster                                                |
| genshi_xml      | 33.8 ms                                                | 35.9 ms: 1.06x slower                                                |
| Geometric mean  | (ref)                                                  | 1.20x faster                                                         |

All benchmarks:
===============

| Benchmark                | bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120 | bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0 |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 323 us                                                 | 103 us: 3.13x faster                                                 |
| deltablue                | 4.91 ms                                                | 2.43 ms: 2.02x faster                                                |
| async_tree_none          | 388 ms                                                 | 198 ms: 1.96x faster                                                 |
| logging_silent           | 117 ns                                                 | 64.2 ns: 1.82x faster                                                |
| raytrace                 | 301 ms                                                 | 169 ms: 1.78x faster                                                 |
| async_tree_memoization   | 474 ms                                                 | 268 ms: 1.77x faster                                                 |
| async_tree_io            | 980 ms                                                 | 558 ms: 1.76x faster                                                 |
| richards_super           | 57.8 ms                                                | 33.8 ms: 1.71x faster                                                |
| richards                 | 48.7 ms                                                | 29.8 ms: 1.63x faster                                                |
| chaos                    | 65.8 ms                                                | 40.4 ms: 1.63x faster                                                |
| sqlglot_parse            | 1.24 ms                                                | 772 us: 1.61x faster                                                 |
| pylint                   | 277 ms                                                 | 177 ms: 1.56x faster                                                 |
| mako                     | 9.87 ms                                                | 6.40 ms: 1.54x faster                                                |
| pickle_pure_python       | 281 us                                                 | 182 us: 1.54x faster                                                 |
| sqlglot_transpile        | 1.44 ms                                                | 942 us: 1.53x faster                                                 |
| asyncio_tcp              | 659 ms                                                 | 431 ms: 1.53x faster                                                 |
| unpickle_pure_python     | 194 us                                                 | 132 us: 1.48x faster                                                 |
| crypto_pyaes             | 71.8 ms                                                | 48.9 ms: 1.47x faster                                                |
| scimark_monte_carlo      | 65.6 ms                                                | 44.7 ms: 1.47x faster                                                |
| go                       | 151 ms                                                 | 104 ms: 1.45x faster                                                 |
| deepcopy_memo            | 34.7 us                                                | 24.1 us: 1.44x faster                                                |
| logging_simple           | 4.45 us                                                | 3.12 us: 1.43x faster                                                |
| logging_format           | 4.83 us                                                | 3.38 us: 1.43x faster                                                |
| async_tree_cpu_io_mixed  | 649 ms                                                 | 457 ms: 1.42x faster                                                 |
| chameleon                | 6.26 ms                                                | 4.45 ms: 1.41x faster                                                |
| tomli_loads              | 1.71 sec                                               | 1.23 sec: 1.38x faster                                               |
| hexiom                   | 6.19 ms                                                | 4.48 ms: 1.38x faster                                                |
| html5lib                 | 42.4 ms                                                | 30.7 ms: 1.38x faster                                                |
| nbody                    | 93.0 ms                                                | 67.9 ms: 1.37x faster                                                |
| pycparser                | 877 ms                                                 | 642 ms: 1.36x faster                                                 |
| float                    | 69.0 ms                                                | 50.7 ms: 1.36x faster                                                |
| spectral_norm            | 94.8 ms                                                | 70.3 ms: 1.35x faster                                                |
| pprint_safe_repr         | 641 ms                                                 | 475 ms: 1.35x faster                                                 |
| pyflate                  | 427 ms                                                 | 317 ms: 1.35x faster                                                 |
| comprehensions           | 16.9 us                                                | 12.6 us: 1.34x faster                                                |
| pprint_pformat           | 1.30 sec                                               | 980 ms: 1.33x faster                                                 |
| regex_compile            | 95.3 ms                                                | 72.1 ms: 1.32x faster                                                |
| thrift                   | 572 us                                                 | 439 us: 1.30x faster                                                 |
| scimark_lu               | 103 ms                                                 | 80.0 ms: 1.29x faster                                                |
| json_dumps               | 8.11 ms                                                | 6.31 ms: 1.28x faster                                                |
| fannkuch                 | 303 ms                                                 | 236 ms: 1.28x faster                                                 |
| xml_etree_process        | 46.5 ms                                                | 36.5 ms: 1.28x faster                                                |
| deepcopy                 | 272 us                                                 | 213 us: 1.27x faster                                                 |
| django_template          | 26.4 ms                                                | 20.8 ms: 1.27x faster                                                |
| coroutines               | 20.7 ms                                                | 16.3 ms: 1.27x faster                                                |
| sympy_sum                | 92.2 ms                                                | 72.8 ms: 1.27x faster                                                |
| deepcopy_reduce          | 2.33 us                                                | 1.86 us: 1.25x faster                                                |
| mypy2                    | 607 ms                                                 | 487 ms: 1.25x faster                                                 |
| scimark_sor              | 128 ms                                                 | 104 ms: 1.23x faster                                                 |
| dulwich_log              | 35.3 ms                                                | 28.8 ms: 1.23x faster                                                |
| asyncio_tcp_ssl          | 1.60 sec                                               | 1.32 sec: 1.21x faster                                               |
| tornado_http             | 86.7 ms                                                | 71.5 ms: 1.21x faster                                                |
| sympy_str                | 165 ms                                                 | 136 ms: 1.21x faster                                                 |
| sympy_integrate          | 13.1 ms                                                | 10.9 ms: 1.21x faster                                                |
| generators               | 32.3 ms                                                | 26.9 ms: 1.20x faster                                                |
| regex_dna                | 174 ms                                                 | 149 ms: 1.17x faster                                                 |
| scimark_fft              | 224 ms                                                 | 192 ms: 1.17x faster                                                 |
| docutils                 | 1.73 sec                                               | 1.50 sec: 1.16x faster                                               |
| sympy_expand             | 269 ms                                                 | 233 ms: 1.16x faster                                                 |
| dask                     | 253 ms                                                 | 221 ms: 1.14x faster                                                 |
| scimark_sparse_mat_mult  | 3.42 ms                                                | 3.03 ms: 1.13x faster                                                |
| aiohttp                  | 1.22 ms                                                | 1.09 ms: 1.13x faster                                                |
| gunicorn                 | 1.30 ms                                                | 1.16 ms: 1.13x faster                                                |
| genshi_text              | 17.3 ms                                                | 15.6 ms: 1.11x faster                                                |
| sqlglot_optimize         | 36.8 ms                                                | 33.3 ms: 1.10x faster                                                |
| nqueens                  | 63.8 ms                                                | 58.3 ms: 1.09x faster                                                |
| bench_thread_pool        | 527 us                                                 | 487 us: 1.08x faster                                                 |
| sqlglot_normalize        | 190 ms                                                 | 176 ms: 1.08x faster                                                 |
| mdp                      | 1.63 sec                                               | 1.52 sec: 1.07x faster                                               |
| meteor_contest           | 77.7 ms                                                | 72.8 ms: 1.07x faster                                                |
| json                     | 3.08 ms                                                | 2.91 ms: 1.06x faster                                                |
| pathlib                  | 24.5 ms                                                | 23.3 ms: 1.05x faster                                                |
| 2to3                     | 192 ms                                                 | 183 ms: 1.04x faster                                                 |
| xml_etree_parse          | 108 ms                                                 | 104 ms: 1.04x faster                                                 |
| xml_etree_iterparse      | 72.1 ms                                                | 70.7 ms: 1.02x faster                                                |
| asyncio_websockets       | 410 ms                                                 | 408 ms: 1.00x faster                                                 |
| xml_etree_generate       | 53.5 ms                                                | 53.6 ms: 1.00x slower                                                |
| regex_v8                 | 17.1 ms                                                | 17.4 ms: 1.01x slower                                                |
| json_loads               | 16.4 us                                                | 17.0 us: 1.04x slower                                                |
| gc_traversal             | 2.36 ms                                                | 2.46 ms: 1.04x slower                                                |
| regex_effbot             | 2.46 ms                                                | 2.58 ms: 1.05x slower                                                |
| unpickle                 | 8.80 us                                                | 9.29 us: 1.06x slower                                                |
| create_gc_cycles         | 860 us                                                 | 908 us: 1.06x slower                                                 |
| genshi_xml               | 33.8 ms                                                | 35.9 ms: 1.06x slower                                                |
| pickle_dict              | 17.0 us                                                | 18.2 us: 1.07x slower                                                |
| pickle                   | 6.97 us                                                | 7.48 us: 1.07x slower                                                |
| sqlite_synth             | 1.46 us                                                | 1.57 us: 1.07x slower                                                |
| unpickle_list            | 2.69 us                                                | 2.91 us: 1.08x slower                                                |
| pickle_list              | 2.74 us                                                | 2.98 us: 1.09x slower                                                |
| coverage                 | 41.5 ms                                                | 45.3 ms: 1.09x slower                                                |
| bench_mp_pool            | 37.4 ms                                                | 46.2 ms: 1.24x slower                                                |
| async_generators         | 231 ms                                                 | 294 ms: 1.27x slower                                                 |
| telco                    | 3.49 ms                                                | 4.46 ms: 1.28x slower                                                |
| python_startup           | 10.9 ms                                                | 14.1 ms: 1.30x slower                                                |
| python_startup_no_site   | 7.91 ms                                                | 11.1 ms: 1.41x slower                                                |
| Geometric mean           | (ref)                                                  | 1.23x faster                                                         |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-darwin-arm64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (12) of results/bm-20240427-3.13.0a6+-b2bbeb0-JIT/bm-20240427-darwin-arm64-savannahostrowski-llvm_18-3.13.0a6+-b2bbeb0.json: async_tree_cpu_io_mixed_tg, async_tree_eager, async_tree_eager_cpu_io_mixed, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io, async_tree_eager_io_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, async_tree_eager_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: 1.40x