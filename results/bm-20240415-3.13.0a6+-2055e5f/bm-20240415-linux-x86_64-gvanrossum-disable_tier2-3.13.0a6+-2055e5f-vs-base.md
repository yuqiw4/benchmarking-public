# Results vs. base

- fork: gvanrossum
- ref: disable_tier2
- machine: linux-x86_64
- commit hash: 2055e5f
- commit date: 2024-04-15
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 270 ms                                                                 | 268 ms: 1.01x faster                                                |
| chameleon      | 7.10 ms                                                                | 6.91 ms: 1.03x faster                                               |
| docutils       | 2.83 sec                                                               | 2.79 sec: 1.01x faster                                              |
| html5lib       | 68.3 ms                                                                | 67.5 ms: 1.01x faster                                               |
| tornado_http   | 94.0 ms                                                                | 94.3 ms: 1.00x slower                                               |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|--------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg | 336 ms                                                                 | 331 ms: 1.02x faster                                                |
| Geometric mean     | (ref)                                                                  | 1.00x faster                                                        |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_io, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 90.1 ms                                                                | 85.7 ms: 1.05x faster                                               |
| float          | 78.5 ms                                                                | 77.7 ms: 1.01x faster                                               |
| pidigits       | 194 ms                                                                 | 198 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 234 ms                                                                 | 226 ms: 1.04x faster                                                |
| regex_effbot   | 3.88 ms                                                                | 3.82 ms: 1.02x faster                                               |
| regex_compile  | 136 ms                                                                 | 134 ms: 1.02x faster                                                |
| regex_v8       | 26.2 ms                                                                | 25.9 ms: 1.01x faster                                               |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_list          | 5.28 us                                                                | 5.00 us: 1.06x faster                                               |
| unpickle_list        | 5.22 us                                                                | 5.07 us: 1.03x faster                                               |
| tomli_loads          | 2.15 sec                                                               | 2.09 sec: 1.03x faster                                              |
| unpickle_pure_python | 218 us                                                                 | 212 us: 1.03x faster                                                |
| pickle               | 12.0 us                                                                | 11.7 us: 1.02x faster                                               |
| pickle_dict          | 34.7 us                                                                | 34.0 us: 1.02x faster                                               |
| xml_etree_process    | 60.9 ms                                                                | 59.9 ms: 1.02x faster                                               |
| pickle_pure_python   | 302 us                                                                 | 298 us: 1.01x faster                                                |
| xml_etree_generate   | 87.9 ms                                                                | 86.9 ms: 1.01x faster                                               |
| json_loads           | 28.0 us                                                                | 27.9 us: 1.00x faster                                               |
| json_dumps           | 10.5 ms                                                                | 10.6 ms: 1.02x slower                                               |
| unpickle             | 15.3 us                                                                | 17.0 us: 1.11x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.11 ms                                                                | 7.12 ms: 1.00x slower                                               |
| python_startup         | 10.5 ms                                                                | 10.6 ms: 1.00x slower                                               |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 11.0 ms                                                                | 10.8 ms: 1.02x faster                                               |
| genshi_text     | 24.0 ms                                                                | 23.7 ms: 1.01x faster                                               |
| genshi_xml      | 52.9 ms                                                                | 52.4 ms: 1.01x faster                                               |
| django_template | 34.8 ms                                                                | 34.4 ms: 1.01x faster                                               |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                        |

All benchmarks:
===============

| Benchmark                | bm-20240415-linux-x86_64-python-0823f4361850145152a9-3.13.0a6+-0823f43 | bm-20240415-linux-x86_64-gvanrossum-disable_tier2-3.13.0a6+-2055e5f |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mdp                      | 2.78 sec                                                               | 2.56 sec: 1.08x faster                                              |
| logging_silent           | 104 ns                                                                 | 96.2 ns: 1.08x faster                                               |
| pickle_list              | 5.28 us                                                                | 5.00 us: 1.06x faster                                               |
| nbody                    | 90.1 ms                                                                | 85.7 ms: 1.05x faster                                               |
| comprehensions           | 16.8 us                                                                | 16.2 us: 1.04x faster                                               |
| hexiom                   | 6.36 ms                                                                | 6.13 ms: 1.04x faster                                               |
| nqueens                  | 82.5 ms                                                                | 79.6 ms: 1.04x faster                                               |
| regex_dna                | 234 ms                                                                 | 226 ms: 1.04x faster                                                |
| deltablue                | 3.25 ms                                                                | 3.14 ms: 1.03x faster                                               |
| richards_super           | 53.7 ms                                                                | 52.2 ms: 1.03x faster                                               |
| unpickle_list            | 5.22 us                                                                | 5.07 us: 1.03x faster                                               |
| deepcopy_memo            | 38.2 us                                                                | 37.1 us: 1.03x faster                                               |
| tomli_loads              | 2.15 sec                                                               | 2.09 sec: 1.03x faster                                              |
| unpickle_pure_python     | 218 us                                                                 | 212 us: 1.03x faster                                                |
| chameleon                | 7.10 ms                                                                | 6.91 ms: 1.03x faster                                               |
| richards                 | 47.5 ms                                                                | 46.3 ms: 1.03x faster                                               |
| djangocms                | 32.1 us                                                                | 31.3 us: 1.03x faster                                               |
| logging_format           | 6.43 us                                                                | 6.26 us: 1.03x faster                                               |
| logging_simple           | 5.79 us                                                                | 5.64 us: 1.03x faster                                               |
| meteor_contest           | 111 ms                                                                 | 109 ms: 1.03x faster                                                |
| pickle                   | 12.0 us                                                                | 11.7 us: 1.02x faster                                               |
| mako                     | 11.0 ms                                                                | 10.8 ms: 1.02x faster                                               |
| go                       | 143 ms                                                                 | 140 ms: 1.02x faster                                                |
| spectral_norm            | 113 ms                                                                 | 111 ms: 1.02x faster                                                |
| pickle_dict              | 34.7 us                                                                | 34.0 us: 1.02x faster                                               |
| scimark_sor              | 123 ms                                                                 | 120 ms: 1.02x faster                                                |
| coverage                 | 98.4 ms                                                                | 96.4 ms: 1.02x faster                                               |
| raytrace                 | 264 ms                                                                 | 259 ms: 1.02x faster                                                |
| sqlglot_optimize         | 55.7 ms                                                                | 54.7 ms: 1.02x faster                                               |
| xml_etree_process        | 60.9 ms                                                                | 59.9 ms: 1.02x faster                                               |
| regex_effbot             | 3.88 ms                                                                | 3.82 ms: 1.02x faster                                               |
| pprint_safe_repr         | 761 ms                                                                 | 749 ms: 1.02x faster                                                |
| regex_compile            | 136 ms                                                                 | 134 ms: 1.02x faster                                                |
| async_tree_none_tg       | 336 ms                                                                 | 331 ms: 1.02x faster                                                |
| scimark_monte_carlo      | 68.3 ms                                                                | 67.3 ms: 1.02x faster                                               |
| docutils                 | 2.83 sec                                                               | 2.79 sec: 1.01x faster                                              |
| regex_v8                 | 26.2 ms                                                                | 25.9 ms: 1.01x faster                                               |
| sqlglot_normalize        | 111 ms                                                                 | 109 ms: 1.01x faster                                                |
| json                     | 5.23 ms                                                                | 5.16 ms: 1.01x faster                                               |
| genshi_text              | 24.0 ms                                                                | 23.7 ms: 1.01x faster                                               |
| pprint_pformat           | 1.55 sec                                                               | 1.53 sec: 1.01x faster                                              |
| dulwich_log              | 66.7 ms                                                                | 65.9 ms: 1.01x faster                                               |
| fannkuch                 | 395 ms                                                                 | 391 ms: 1.01x faster                                                |
| pickle_pure_python       | 302 us                                                                 | 298 us: 1.01x faster                                                |
| html5lib                 | 68.3 ms                                                                | 67.5 ms: 1.01x faster                                               |
| sqlglot_parse            | 1.28 ms                                                                | 1.27 ms: 1.01x faster                                               |
| deepcopy_reduce          | 3.20 us                                                                | 3.16 us: 1.01x faster                                               |
| sympy_integrate          | 20.4 ms                                                                | 20.2 ms: 1.01x faster                                               |
| xml_etree_generate       | 87.9 ms                                                                | 86.9 ms: 1.01x faster                                               |
| genshi_xml               | 52.9 ms                                                                | 52.4 ms: 1.01x faster                                               |
| django_template          | 34.8 ms                                                                | 34.4 ms: 1.01x faster                                               |
| float                    | 78.5 ms                                                                | 77.7 ms: 1.01x faster                                               |
| crypto_pyaes             | 75.5 ms                                                                | 74.8 ms: 1.01x faster                                               |
| chaos                    | 59.9 ms                                                                | 59.5 ms: 1.01x faster                                               |
| 2to3                     | 270 ms                                                                 | 268 ms: 1.01x faster                                                |
| sympy_sum                | 155 ms                                                                 | 154 ms: 1.01x faster                                                |
| sqlite_synth             | 2.95 us                                                                | 2.94 us: 1.01x faster                                               |
| sqlglot_transpile        | 1.60 ms                                                                | 1.59 ms: 1.01x faster                                               |
| scimark_sparse_mat_mult  | 5.20 ms                                                                | 5.17 ms: 1.00x faster                                               |
| json_loads               | 28.0 us                                                                | 27.9 us: 1.00x faster                                               |
| deepcopy                 | 353 us                                                                 | 351 us: 1.00x faster                                                |
| asyncio_tcp_ssl          | 1.84 sec                                                               | 1.84 sec: 1.00x faster                                              |
| python_startup_no_site   | 7.11 ms                                                                | 7.12 ms: 1.00x slower                                               |
| python_startup           | 10.5 ms                                                                | 10.6 ms: 1.00x slower                                               |
| tornado_http             | 94.0 ms                                                                | 94.3 ms: 1.00x slower                                               |
| create_gc_cycles         | 1.74 ms                                                                | 1.75 ms: 1.01x slower                                               |
| generators               | 29.2 ms                                                                | 29.4 ms: 1.01x slower                                               |
| scimark_fft              | 366 ms                                                                 | 369 ms: 1.01x slower                                                |
| typing_runtime_protocols | 113 us                                                                 | 115 us: 1.01x slower                                                |
| scimark_lu               | 113 ms                                                                 | 115 ms: 1.02x slower                                                |
| json_dumps               | 10.5 ms                                                                | 10.6 ms: 1.02x slower                                               |
| coroutines               | 22.7 ms                                                                | 23.1 ms: 1.02x slower                                               |
| pidigits                 | 194 ms                                                                 | 198 ms: 1.02x slower                                                |
| gc_traversal             | 3.75 ms                                                                | 4.01 ms: 1.07x slower                                               |
| unpickle                 | 15.3 us                                                                | 17.0 us: 1.11x slower                                               |
| Geometric mean           | (ref)                                                                  | 1.01x faster                                                        |

Benchmark hidden because not significant (26): async_tree_io_tg, pycparser, bench_thread_pool, async_tree_memoization_tg, dask, pylint, async_tree_cpu_io_mixed_tg, xml_etree_iterparse, sympy_str, asyncio_websockets, sympy_expand, aiohttp, async_tree_cpu_io_mixed, async_tree_none, gunicorn, asyncio_tcp, async_generators, telco, mypy2, bench_mp_pool, pyflate, thrift, pathlib, async_tree_io, async_tree_memoization, xml_etree_parse

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x