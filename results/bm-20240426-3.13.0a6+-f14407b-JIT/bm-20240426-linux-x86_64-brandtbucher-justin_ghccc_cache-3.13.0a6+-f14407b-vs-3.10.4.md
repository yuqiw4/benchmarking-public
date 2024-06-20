# Results vs. 3.10.4

- fork: brandtbucher
- ref: justin_ghccc_cache
- machine: linux-x86_64
- commit hash: f14407b
- commit date: 2024-04-26
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 348 ms                                                 | 275 ms: 1.27x faster                                                       |
| chameleon      | 9.68 ms                                                | 7.04 ms: 1.38x faster                                                      |
| docutils       | 3.30 sec                                               | 2.93 sec: 1.12x faster                                                     |
| html5lib       | 88.9 ms                                                | 68.1 ms: 1.30x faster                                                      |
| tornado_http   | 136 ms                                                 | 95.6 ms: 1.43x faster                                                      |
| Geometric mean | (ref)                                                  | 1.30x faster                                                               |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|-------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_none         | 728 ms                                                 | 355 ms: 2.05x faster                                                       |
| async_tree_io           | 1.77 sec                                               | 921 ms: 1.92x faster                                                       |
| async_tree_memoization  | 870 ms                                                 | 463 ms: 1.88x faster                                                       |
| async_tree_cpu_io_mixed | 1.02 sec                                               | 614 ms: 1.65x faster                                                       |
| Geometric mean          | (ref)                                                  | 1.87x faster                                                               |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| nbody          | 154 ms                                                 | 80.0 ms: 1.92x faster                                                      |
| float          | 117 ms                                                 | 73.1 ms: 1.60x faster                                                      |
| pidigits       | 191 ms                                                 | 210 ms: 1.10x slower                                                       |
| Geometric mean | (ref)                                                  | 1.41x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 188 ms                                                 | 141 ms: 1.34x faster                                                       |
| regex_v8       | 27.8 ms                                                | 24.7 ms: 1.12x faster                                                      |
| regex_dna      | 227 ms                                                 | 225 ms: 1.01x faster                                                       |
| regex_effbot   | 3.63 ms                                                | 4.23 ms: 1.17x slower                                                      |
| Geometric mean | (ref)                                                  | 1.07x faster                                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| tomli_loads          | 3.14 sec                                               | 1.93 sec: 1.62x faster                                                     |
| pickle_pure_python   | 484 us                                                 | 308 us: 1.57x faster                                                       |
| unpickle_pure_python | 331 us                                                 | 226 us: 1.46x faster                                                       |
| json_dumps           | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                      |
| xml_etree_process    | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                      |
| xml_etree_generate   | 99.4 ms                                                | 86.8 ms: 1.15x faster                                                      |
| json_loads           | 31.2 us                                                | 27.4 us: 1.14x faster                                                      |
| xml_etree_iterparse  | 115 ms                                                 | 102 ms: 1.13x faster                                                       |
| xml_etree_parse      | 168 ms                                                 | 149 ms: 1.13x faster                                                       |
| unpickle             | 14.4 us                                                | 15.5 us: 1.08x slower                                                      |
| pickle               | 10.7 us                                                | 12.0 us: 1.12x slower                                                      |
| pickle_dict          | 29.6 us                                                | 34.8 us: 1.18x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.16x faster                                                               |

Benchmark hidden because not significant (2): unpickle_list, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                      |
| python_startup_no_site | 5.93 ms                                                | 7.66 ms: 1.29x slower                                                      |
| Geometric mean         | (ref)                                                  | 1.01x faster                                                               |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| mako            | 16.3 ms                                                | 10.0 ms: 1.63x faster                                                      |
| django_template | 48.2 ms                                                | 36.7 ms: 1.31x faster                                                      |
| genshi_text     | 31.8 ms                                                | 25.0 ms: 1.27x faster                                                      |
| genshi_xml      | 66.0 ms                                                | 54.1 ms: 1.22x faster                                                      |
| Geometric mean  | (ref)                                                  | 1.35x faster                                                               |

All benchmarks:
===============

| Benchmark                | bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120 | bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b |
|--------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------:|
| typing_runtime_protocols | 544 us                                                 | 117 us: 4.66x faster                                                       |
| generators               | 80.1 ms                                                | 29.8 ms: 2.69x faster                                                      |
| deltablue                | 7.91 ms                                                | 3.72 ms: 2.13x faster                                                      |
| async_tree_none          | 728 ms                                                 | 355 ms: 2.05x faster                                                       |
| richards_super           | 94.7 ms                                                | 48.9 ms: 1.94x faster                                                      |
| nbody                    | 154 ms                                                 | 80.0 ms: 1.92x faster                                                      |
| async_tree_io            | 1.77 sec                                               | 921 ms: 1.92x faster                                                       |
| chaos                    | 115 ms                                                 | 61.0 ms: 1.89x faster                                                      |
| scimark_monte_carlo      | 118 ms                                                 | 62.5 ms: 1.89x faster                                                      |
| crypto_pyaes             | 128 ms                                                 | 67.6 ms: 1.89x faster                                                      |
| async_tree_memoization   | 870 ms                                                 | 463 ms: 1.88x faster                                                       |
| richards                 | 79.3 ms                                                | 42.4 ms: 1.87x faster                                                      |
| raytrace                 | 507 ms                                                 | 274 ms: 1.85x faster                                                       |
| logging_silent           | 190 ns                                                 | 104 ns: 1.83x faster                                                       |
| asyncio_tcp              | 922 ms                                                 | 513 ms: 1.80x faster                                                       |
| spectral_norm            | 170 ms                                                 | 99.2 ms: 1.71x faster                                                      |
| scimark_sor              | 220 ms                                                 | 128 ms: 1.71x faster                                                       |
| comprehensions           | 28.8 us                                                | 17.2 us: 1.67x faster                                                      |
| pylint                   | 551 ms                                                 | 332 ms: 1.66x faster                                                       |
| sqlglot_parse            | 2.17 ms                                                | 1.31 ms: 1.66x faster                                                      |
| async_tree_cpu_io_mixed  | 1.02 sec                                               | 614 ms: 1.65x faster                                                       |
| pyflate                  | 716 ms                                                 | 434 ms: 1.65x faster                                                       |
| go                       | 240 ms                                                 | 147 ms: 1.63x faster                                                       |
| mako                     | 16.3 ms                                                | 10.0 ms: 1.63x faster                                                      |
| tomli_loads              | 3.14 sec                                               | 1.93 sec: 1.62x faster                                                     |
| float                    | 117 ms                                                 | 73.1 ms: 1.60x faster                                                      |
| hexiom                   | 10.4 ms                                                | 6.57 ms: 1.58x faster                                                      |
| sqlglot_transpile        | 2.57 ms                                                | 1.63 ms: 1.58x faster                                                      |
| pickle_pure_python       | 484 us                                                 | 308 us: 1.57x faster                                                       |
| coroutines               | 35.1 ms                                                | 22.8 ms: 1.54x faster                                                      |
| scimark_fft              | 466 ms                                                 | 310 ms: 1.50x faster                                                       |
| fannkuch                 | 532 ms                                                 | 357 ms: 1.49x faster                                                       |
| deepcopy_memo            | 58.5 us                                                | 39.8 us: 1.47x faster                                                      |
| unpickle_pure_python     | 331 us                                                 | 226 us: 1.46x faster                                                       |
| pprint_pformat           | 2.10 sec                                               | 1.46 sec: 1.44x faster                                                     |
| tornado_http             | 136 ms                                                 | 95.6 ms: 1.43x faster                                                      |
| scimark_sparse_mat_mult  | 6.47 ms                                                | 4.55 ms: 1.42x faster                                                      |
| pprint_safe_repr         | 1.02 sec                                               | 722 ms: 1.41x faster                                                       |
| scimark_lu               | 176 ms                                                 | 125 ms: 1.40x faster                                                       |
| logging_simple           | 8.30 us                                                | 5.92 us: 1.40x faster                                                      |
| logging_format           | 9.09 us                                                | 6.52 us: 1.39x faster                                                      |
| asyncio_tcp_ssl          | 2.57 sec                                               | 1.86 sec: 1.38x faster                                                     |
| chameleon                | 9.68 ms                                                | 7.04 ms: 1.38x faster                                                      |
| pycparser                | 1.58 sec                                               | 1.16 sec: 1.36x faster                                                     |
| regex_compile            | 188 ms                                                 | 141 ms: 1.34x faster                                                       |
| deepcopy                 | 479 us                                                 | 362 us: 1.32x faster                                                       |
| json_dumps               | 14.2 ms                                                | 10.7 ms: 1.32x faster                                                      |
| xml_etree_process        | 79.1 ms                                                | 60.0 ms: 1.32x faster                                                      |
| python_startup           | 14.6 ms                                                | 11.1 ms: 1.32x faster                                                      |
| django_template          | 48.2 ms                                                | 36.7 ms: 1.31x faster                                                      |
| html5lib                 | 88.9 ms                                                | 68.1 ms: 1.30x faster                                                      |
| deepcopy_reduce          | 4.17 us                                                | 3.20 us: 1.30x faster                                                      |
| thrift                   | 1.07 ms                                                | 834 us: 1.29x faster                                                       |
| genshi_text              | 31.8 ms                                                | 25.0 ms: 1.27x faster                                                      |
| 2to3                     | 348 ms                                                 | 275 ms: 1.27x faster                                                       |
| sqlglot_normalize        | 143 ms                                                 | 113 ms: 1.26x faster                                                       |
| genshi_xml               | 66.0 ms                                                | 54.1 ms: 1.22x faster                                                      |
| sqlglot_optimize         | 69.2 ms                                                | 57.1 ms: 1.21x faster                                                      |
| dulwich_log              | 84.3 ms                                                | 69.7 ms: 1.21x faster                                                      |
| nqueens                  | 106 ms                                                 | 87.5 ms: 1.21x faster                                                      |
| djangocms                | 38.4 us                                                | 32.2 us: 1.19x faster                                                      |
| aiohttp                  | 1.44 ms                                                | 1.21 ms: 1.19x faster                                                      |
| sympy_sum                | 196 ms                                                 | 166 ms: 1.18x faster                                                       |
| dask                     | 441 ms                                                 | 373 ms: 1.18x faster                                                       |
| sympy_str                | 346 ms                                                 | 294 ms: 1.18x faster                                                       |
| sympy_integrate          | 25.8 ms                                                | 21.9 ms: 1.18x faster                                                      |
| gunicorn                 | 1.53 ms                                                | 1.30 ms: 1.17x faster                                                      |
| xml_etree_generate       | 99.4 ms                                                | 86.8 ms: 1.15x faster                                                      |
| pathlib                  | 20.5 ms                                                | 17.9 ms: 1.15x faster                                                      |
| bench_thread_pool        | 986 us                                                 | 863 us: 1.14x faster                                                       |
| sympy_expand             | 566 ms                                                 | 496 ms: 1.14x faster                                                       |
| mypy2                    | 894 ms                                                 | 785 ms: 1.14x faster                                                       |
| json_loads               | 31.2 us                                                | 27.4 us: 1.14x faster                                                      |
| xml_etree_iterparse      | 115 ms                                                 | 102 ms: 1.13x faster                                                       |
| xml_etree_parse          | 168 ms                                                 | 149 ms: 1.13x faster                                                       |
| docutils                 | 3.30 sec                                               | 2.93 sec: 1.12x faster                                                     |
| regex_v8                 | 27.8 ms                                                | 24.7 ms: 1.12x faster                                                      |
| json                     | 5.69 ms                                                | 5.13 ms: 1.11x faster                                                      |
| meteor_contest           | 120 ms                                                 | 110 ms: 1.09x faster                                                       |
| sqlite_synth             | 3.02 us                                                | 2.83 us: 1.07x faster                                                      |
| mdp                      | 2.85 sec                                               | 2.79 sec: 1.02x faster                                                     |
| regex_dna                | 227 ms                                                 | 225 ms: 1.01x faster                                                       |
| asyncio_websockets       | 559 ms                                                 | 564 ms: 1.01x slower                                                       |
| async_generators         | 444 ms                                                 | 470 ms: 1.06x slower                                                       |
| gc_traversal             | 3.62 ms                                                | 3.86 ms: 1.07x slower                                                      |
| create_gc_cycles         | 1.62 ms                                                | 1.75 ms: 1.08x slower                                                      |
| unpickle                 | 14.4 us                                                | 15.5 us: 1.08x slower                                                      |
| pidigits                 | 191 ms                                                 | 210 ms: 1.10x slower                                                       |
| pickle                   | 10.7 us                                                | 12.0 us: 1.12x slower                                                      |
| regex_effbot             | 3.63 ms                                                | 4.23 ms: 1.17x slower                                                      |
| pickle_dict              | 29.6 us                                                | 34.8 us: 1.18x slower                                                      |
| telco                    | 7.27 ms                                                | 8.74 ms: 1.20x slower                                                      |
| coverage                 | 79.4 ms                                                | 98.1 ms: 1.23x slower                                                      |
| python_startup_no_site   | 5.93 ms                                                | 7.66 ms: 1.29x slower                                                      |
| Geometric mean           | (ref)                                                  | 1.34x faster                                                               |

Benchmark hidden because not significant (3): unpickle_list, bench_mp_pool, pickle_list
Ignored benchmarks (4) of results/bm-20220323-3.10.4-9d38120/bm-20220323-linux-x86_64-python-v3.10.4-3.10.4-9d38120.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (4) of results/bm-20240426-3.13.0a6+-f14407b-JIT/bm-20240426-linux-x86_64-brandtbucher-justin_ghccc_cache-3.13.0a6+-f14407b.json: async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.27x
- 95% likely to have a speedup of 1.26x
- 99% likely to have a speedup of 1.21x

# Memory
- memory change: 1.22x