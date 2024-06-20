# Results vs. 3.13.0b2

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.00x faster
- HPT reliability: 86.42%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 274 ms                                                     | 276 ms: 1.01x slower                                                 |
| chameleon      | 7.22 ms                                                    | 7.05 ms: 1.02x faster                                                |
| docutils       | 2.83 sec                                                   | 2.90 sec: 1.02x slower                                               |
| html5lib       | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                                |
| tornado_http   | 94.6 ms                                                    | 97.0 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                      | 1.01x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|--------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none    | 378 ms                                                     | 356 ms: 1.06x faster                                                 |
| async_tree_io_tg   | 936 ms                                                     | 907 ms: 1.03x faster                                                 |
| async_tree_none_tg | 336 ms                                                     | 347 ms: 1.03x slower                                                 |
| Geometric mean     | (ref)                                                      | 1.01x faster                                                         |

Benchmark hidden because not significant (5): async_tree_memoization, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 78.9 ms                                                    | 72.8 ms: 1.08x faster                                                |
| nbody          | 88.3 ms                                                    | 87.0 ms: 1.02x faster                                                |
| pidigits       | 191 ms                                                     | 189 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                      | 1.04x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.67 ms                                                    | 3.63 ms: 1.01x faster                                                |
| regex_dna      | 221 ms                                                     | 219 ms: 1.01x faster                                                 |
| regex_v8       | 25.1 ms                                                    | 25.0 ms: 1.00x faster                                                |
| regex_compile  | 137 ms                                                     | 143 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                      | 1.00x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 2.12 sec                                                   | 2.02 sec: 1.05x faster                                               |
| pickle_list          | 5.11 us                                                    | 4.97 us: 1.03x faster                                                |
| unpickle_list        | 5.34 us                                                    | 5.23 us: 1.02x faster                                                |
| xml_etree_process    | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                |
| pickle_dict          | 34.8 us                                                    | 34.2 us: 1.02x faster                                                |
| xml_etree_iterparse  | 107 ms                                                     | 106 ms: 1.01x faster                                                 |
| xml_etree_generate   | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                |
| json_dumps           | 10.7 ms                                                    | 10.7 ms: 1.01x faster                                                |
| pickle_pure_python   | 305 us                                                     | 308 us: 1.01x slower                                                 |
| pickle               | 11.5 us                                                    | 11.8 us: 1.03x slower                                                |
| unpickle_pure_python | 218 us                                                     | 229 us: 1.05x slower                                                 |
| Geometric mean       | (ref)                                                      | 1.01x faster                                                         |

Benchmark hidden because not significant (3): xml_etree_parse, json_loads, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                |
| python_startup_no_site | 7.11 ms                                                    | 9.49 ms: 1.34x slower                                                |
| Geometric mean         | (ref)                                                      | 1.17x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.2 ms                                                    | 9.96 ms: 1.13x faster                                                |
| django_template | 34.8 ms                                                    | 36.4 ms: 1.05x slower                                                |
| genshi_text     | 23.7 ms                                                    | 24.9 ms: 1.05x slower                                                |
| genshi_xml      | 51.6 ms                                                    | 55.4 ms: 1.07x slower                                                |
| Geometric mean  | (ref)                                                      | 1.01x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 | bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|--------------------------|:----------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols | 165 us                                                     | 114 us: 1.45x faster                                                 |
| scimark_fft              | 392 ms                                                     | 319 ms: 1.23x faster                                                 |
| scimark_sparse_mat_mult  | 5.27 ms                                                    | 4.33 ms: 1.22x faster                                                |
| spectral_norm            | 116 ms                                                     | 101 ms: 1.15x faster                                                 |
| mako                     | 11.2 ms                                                    | 9.96 ms: 1.13x faster                                                |
| richards_super           | 57.4 ms                                                    | 51.7 ms: 1.11x faster                                                |
| richards                 | 50.9 ms                                                    | 46.0 ms: 1.11x faster                                                |
| crypto_pyaes             | 77.5 ms                                                    | 70.1 ms: 1.11x faster                                                |
| fannkuch                 | 402 ms                                                     | 367 ms: 1.10x faster                                                 |
| create_gc_cycles         | 1.82 ms                                                    | 1.66 ms: 1.09x faster                                                |
| float                    | 78.9 ms                                                    | 72.8 ms: 1.08x faster                                                |
| gc_traversal             | 3.98 ms                                                    | 3.69 ms: 1.08x faster                                                |
| pyflate                  | 484 ms                                                     | 451 ms: 1.07x faster                                                 |
| scimark_monte_carlo      | 69.2 ms                                                    | 64.9 ms: 1.07x faster                                                |
| async_tree_none          | 378 ms                                                     | 356 ms: 1.06x faster                                                 |
| pylint                   | 317 ms                                                     | 299 ms: 1.06x faster                                                 |
| mdp                      | 2.79 sec                                                   | 2.64 sec: 1.06x faster                                               |
| tomli_loads              | 2.12 sec                                                   | 2.02 sec: 1.05x faster                                               |
| sqlite_synth             | 2.99 us                                                    | 2.84 us: 1.05x faster                                                |
| deepcopy_reduce          | 3.35 us                                                    | 3.23 us: 1.04x faster                                                |
| coroutines               | 23.2 ms                                                    | 22.4 ms: 1.04x faster                                                |
| async_tree_io_tg         | 936 ms                                                     | 907 ms: 1.03x faster                                                 |
| pprint_pformat           | 1.56 sec                                                   | 1.51 sec: 1.03x faster                                               |
| pprint_safe_repr         | 758 ms                                                     | 738 ms: 1.03x faster                                                 |
| pickle_list              | 5.11 us                                                    | 4.97 us: 1.03x faster                                                |
| chameleon                | 7.22 ms                                                    | 7.05 ms: 1.02x faster                                                |
| unpickle_list            | 5.34 us                                                    | 5.23 us: 1.02x faster                                                |
| xml_etree_process        | 61.2 ms                                                    | 60.0 ms: 1.02x faster                                                |
| chaos                    | 61.3 ms                                                    | 60.3 ms: 1.02x faster                                                |
| pickle_dict              | 34.8 us                                                    | 34.2 us: 1.02x faster                                                |
| nbody                    | 88.3 ms                                                    | 87.0 ms: 1.02x faster                                                |
| pidigits                 | 191 ms                                                     | 189 ms: 1.01x faster                                                 |
| regex_effbot             | 3.67 ms                                                    | 3.63 ms: 1.01x faster                                                |
| deepcopy                 | 367 us                                                     | 363 us: 1.01x faster                                                 |
| xml_etree_iterparse      | 107 ms                                                     | 106 ms: 1.01x faster                                                 |
| logging_silent           | 105 ns                                                     | 104 ns: 1.01x faster                                                 |
| regex_dna                | 221 ms                                                     | 219 ms: 1.01x faster                                                 |
| xml_etree_generate       | 87.4 ms                                                    | 86.7 ms: 1.01x faster                                                |
| json_dumps               | 10.7 ms                                                    | 10.7 ms: 1.01x faster                                                |
| meteor_contest           | 110 ms                                                     | 109 ms: 1.01x faster                                                 |
| regex_v8                 | 25.1 ms                                                    | 25.0 ms: 1.00x faster                                                |
| asyncio_tcp              | 508 ms                                                     | 510 ms: 1.00x slower                                                 |
| sqlglot_parse            | 1.32 ms                                                    | 1.33 ms: 1.00x slower                                                |
| asyncio_websockets       | 567 ms                                                     | 570 ms: 1.01x slower                                                 |
| asyncio_tcp_ssl          | 1.84 sec                                                   | 1.85 sec: 1.01x slower                                               |
| generators               | 29.6 ms                                                    | 29.8 ms: 1.01x slower                                                |
| pickle_pure_python       | 305 us                                                     | 308 us: 1.01x slower                                                 |
| 2to3                     | 274 ms                                                     | 276 ms: 1.01x slower                                                 |
| sqlglot_transpile        | 1.63 ms                                                    | 1.65 ms: 1.01x slower                                                |
| html5lib                 | 67.2 ms                                                    | 68.0 ms: 1.01x slower                                                |
| logging_format           | 6.47 us                                                    | 6.57 us: 1.01x slower                                                |
| telco                    | 8.41 ms                                                    | 8.55 ms: 1.02x slower                                                |
| dask                     | 369 ms                                                     | 376 ms: 1.02x slower                                                 |
| docutils                 | 2.83 sec                                                   | 2.90 sec: 1.02x slower                                               |
| tornado_http             | 94.6 ms                                                    | 97.0 ms: 1.03x slower                                                |
| python_startup           | 10.8 ms                                                    | 11.0 ms: 1.03x slower                                                |
| bench_thread_pool        | 834 us                                                     | 858 us: 1.03x slower                                                 |
| pycparser                | 1.16 sec                                                   | 1.19 sec: 1.03x slower                                               |
| aiohttp                  | 1.18 ms                                                    | 1.22 ms: 1.03x slower                                                |
| pickle                   | 11.5 us                                                    | 11.8 us: 1.03x slower                                                |
| gunicorn                 | 1.28 ms                                                    | 1.32 ms: 1.03x slower                                                |
| async_tree_none_tg       | 336 ms                                                     | 347 ms: 1.03x slower                                                 |
| sympy_str                | 282 ms                                                     | 291 ms: 1.03x slower                                                 |
| logging_simple           | 5.74 us                                                    | 5.94 us: 1.03x slower                                                |
| json                     | 5.31 ms                                                    | 5.50 ms: 1.04x slower                                                |
| coverage                 | 93.1 ms                                                    | 96.9 ms: 1.04x slower                                                |
| django_template          | 34.8 ms                                                    | 36.4 ms: 1.05x slower                                                |
| regex_compile            | 137 ms                                                     | 143 ms: 1.05x slower                                                 |
| raytrace                 | 267 ms                                                     | 279 ms: 1.05x slower                                                 |
| sqlglot_normalize        | 110 ms                                                     | 115 ms: 1.05x slower                                                 |
| unpickle_pure_python     | 218 us                                                     | 229 us: 1.05x slower                                                 |
| comprehensions           | 16.6 us                                                    | 17.4 us: 1.05x slower                                                |
| genshi_text              | 23.7 ms                                                    | 24.9 ms: 1.05x slower                                                |
| sympy_expand             | 473 ms                                                     | 497 ms: 1.05x slower                                                 |
| sympy_sum                | 156 ms                                                     | 164 ms: 1.05x slower                                                 |
| sqlglot_optimize         | 55.5 ms                                                    | 58.7 ms: 1.06x slower                                                |
| async_generators         | 442 ms                                                     | 468 ms: 1.06x slower                                                 |
| sympy_integrate          | 20.5 ms                                                    | 21.7 ms: 1.06x slower                                                |
| scimark_sor              | 127 ms                                                     | 136 ms: 1.06x slower                                                 |
| dulwich_log              | 67.2 ms                                                    | 71.6 ms: 1.07x slower                                                |
| scimark_lu               | 122 ms                                                     | 130 ms: 1.07x slower                                                 |
| mypy2                    | 742 ms                                                     | 794 ms: 1.07x slower                                                 |
| deltablue                | 3.25 ms                                                    | 3.48 ms: 1.07x slower                                                |
| genshi_xml               | 51.6 ms                                                    | 55.4 ms: 1.07x slower                                                |
| hexiom                   | 6.30 ms                                                    | 6.88 ms: 1.09x slower                                                |
| go                       | 145 ms                                                     | 158 ms: 1.09x slower                                                 |
| pathlib                  | 17.3 ms                                                    | 19.1 ms: 1.10x slower                                                |
| nqueens                  | 81.4 ms                                                    | 91.2 ms: 1.12x slower                                                |
| python_startup_no_site   | 7.11 ms                                                    | 9.49 ms: 1.34x slower                                                |
| Geometric mean           | (ref)                                                      | 1.00x faster                                                         |

Benchmark hidden because not significant (12): async_tree_memoization, async_tree_io, djangocms, xml_etree_parse, json_loads, thrift, unpickle, async_tree_cpu_io_mixed, bench_mp_pool, async_tree_memoization_tg, deepcopy_memo, async_tree_cpu_io_mixed_tg
Ignored benchmarks (2) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-linux-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser, flaskblogging
Ignored benchmarks (1) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: unpack_sequence

# HPT report

- Reliability score: 86.42% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.06x