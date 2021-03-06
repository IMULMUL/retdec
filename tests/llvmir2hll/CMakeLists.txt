
add_executable(tests-llvmir2hll
	analysis/alias_analysis/alias_analyses/simple_alias_analysis_tests.cpp
	analysis/break_in_if_analysis_tests.cpp
	analysis/goto_target_analysis_tests.cpp
	analysis/indirect_func_ref_analysis_tests.cpp
	analysis/null_pointer_analysis_tests.cpp
	analysis/value_analysis_tests.cpp
	analysis/var_uses_visitor_tests.cpp
	analysis/written_into_globals_visitor_tests.cpp
	config/config_tests.cpp
	config/configs/json_config_tests.cpp
	evaluator/arithm_expr_evaluators/c_arithm_expr_evaluator_tests.cpp
	evaluator/arithm_expr_evaluators/strict_arithm_expr_evaluator_tests.cpp
	graphs/cfg/cfg_builders/non_recursive_cfg_builder_tests.cpp
	graphs/cfg/cfg_traversals/lhs_rhs_uses_cfg_traversal_tests.cpp
	hll/bracket_managers/c_bracket_manager_tests.cpp
	hll/bracket_managers/no_bracket_manager_tests.cpp
	hll/compound_op_managers/c_compound_op_manager_tests.cpp
	hll/compound_op_managers/compound_op_manager_tests.cpp
	hll/compound_op_managers/no_compound_op_manager_tests.cpp
	hll/hll_writers/c_hll_writer_tests.cpp
	hll/hll_writers/hll_writer_tests.cpp
	hll/output_managers/json_manager_tests.cpp
	hll/output_managers/output_manager_tests.cpp
	hll/output_managers/plain_manager_tests.cpp
	ir/array_index_op_expr_tests.cpp
	ir/array_type_tests.cpp
	ir/assign_stmt_tests.cpp
	ir/call_expr_tests.cpp
	ir/call_stmt_tests.cpp
	ir/const_array_tests.cpp
	ir/const_bool_tests.cpp
	ir/const_float_tests.cpp
	ir/const_int_tests.cpp
	ir/const_string_tests.cpp
	ir/const_symbol_tests.cpp
	ir/expression_tests.cpp
	ir/function_builder_tests.cpp
	ir/function_tests.cpp
	ir/function_type_tests.cpp
	ir/global_var_def_tests.cpp
	ir/if_stmt_tests.cpp
	ir/int_type_tests.cpp
	ir/module_tests.cpp
	ir/return_stmt_tests.cpp
	ir/statement_tests.cpp
	ir/string_type_tests.cpp
	ir/struct_type_tests.cpp
	ir/switch_stmt_tests.cpp
	ir/tests_with_module.cpp
	ir/ufor_loop_stmt.cpp
	ir/unknown_type_tests.cpp
	ir/variable_tests.cpp
	ir/void_type_tests.cpp
	llvm/llvm_intrinsic_converter_tests.cpp
	llvm/llvm_support_tests.cpp
	llvm/llvmir2bir_converter/basic_block_converter_tests.cpp
	llvm/llvmir2bir_converter/cfg_node_tests.cpp
	llvm/llvmir2bir_converter/labels_handler_tests.cpp
	llvm/llvmir2bir_converter/llvm_value_converter_tests/llvm_constant_converter_tests.cpp
	llvm/llvmir2bir_converter/llvm_value_converter_tests/llvm_constant_converter_tests_by_llvmir.cpp
	llvm/llvmir2bir_converter/llvm_value_converter_tests/llvm_fcmp_converter_constants_tests.cpp
	llvm/llvmir2bir_converter/llvm_value_converter_tests/llvm_fcmp_converter_tests.cpp
	llvm/llvmir2bir_converter/llvm_value_converter_tests/llvm_instruction_converter_constants_tests.cpp
	llvm/llvmir2bir_converter/llvm_value_converter_tests/llvm_instruction_converter_tests.cpp
	llvm/llvmir2bir_converter/llvm_value_converter_tests/llvm_type_converter_tests.cpp
	llvm/llvmir2bir_converter/llvm_value_converter_tests/tests_with_llvm_value_converter.cpp
	llvm/llvmir2bir_converter/structure_converter_tests.cpp
	llvm/llvmir2bir_converter/variables_manager_tests.cpp
	llvm/llvmir2bir_converter_tests/base_tests.cpp
	llvm/llvmir2bir_converter_tests/functions_tests.cpp
	llvm/llvmir2bir_converter_tests/glob_vars_tests.cpp
	llvm/string_conversions_tests.cpp
	optimizer/optimizers/bit_op_to_log_op_optimizer_tests.cpp
	optimizer/optimizers/bit_shift_optimizer_tests.cpp
	optimizer/optimizers/break_continue_return_optimizer_tests.cpp
	optimizer/optimizers/c_array_arg_optimizer_tests.cpp
	optimizer/optimizers/copy_propagation_optimizer_tests.cpp
	optimizer/optimizers/dead_code_optimizer_tests.cpp
	optimizer/optimizers/dead_local_assign_optimizer_tests.cpp
	optimizer/optimizers/deref_address_optimizer_tests.cpp
	optimizer/optimizers/deref_to_array_index_optimizer_tests.cpp
	optimizer/optimizers/empty_array_to_string_optimizer_tests.cpp
	optimizer/optimizers/empty_stmt_optimizer_tests.cpp
	optimizer/optimizers/goto_stmt_optimizer_tests.cpp
	optimizer/optimizers/if_before_loop_optimizer_tests.cpp
	optimizer/optimizers/if_structure_optimizer_tests.cpp
	optimizer/optimizers/if_to_switch_optimizer_tests.cpp
	optimizer/optimizers/llvm_intrinsics_optimizer_tests.cpp
	optimizer/optimizers/loop_last_continue_optimizer_tests.cpp
	optimizer/optimizers/no_init_var_def_optimizer_tests.cpp
	optimizer/optimizers/pre_while_true_loop_conv_optimizer_tests.cpp
	optimizer/optimizers/remove_all_casts_optimizer_tests.cpp
	optimizer/optimizers/remove_useless_casts_optimizer_tests.cpp
	optimizer/optimizers/self_assign_optimizer_tests.cpp
	optimizer/optimizers/simple_copy_propagation_optimizer_tests.cpp
	optimizer/optimizers/simplify_arithm_expr/bool_comparison_optimizer_tests.cpp
	optimizer/optimizers/simplify_arithm_expr/change_order_of_operands_sub_optimizer_tests.cpp
	optimizer/optimizers/simplify_arithm_expr/const_operator_const_sub_optimizer_tests.cpp
	optimizer/optimizers/simplify_arithm_expr/equal_operands_sub_optimizer_tests.cpp
	optimizer/optimizers/simplify_arithm_expr/negation_operator_sub_optimizer_tests.cpp
	optimizer/optimizers/simplify_arithm_expr/negative_operand_sub_optimizer_tests.cpp
	optimizer/optimizers/simplify_arithm_expr/one_sub_optimizer_tests.cpp
	optimizer/optimizers/simplify_arithm_expr/ternary_operator_sub_optimizer_tests.cpp
	optimizer/optimizers/simplify_arithm_expr/three_operands_sub_optimizer_tests.cpp
	optimizer/optimizers/simplify_arithm_expr/zero_sub_optimizer_tests.cpp
	optimizer/optimizers/simplify_arithm_expr_optimizer_tests.cpp
	optimizer/optimizers/unused_global_var_optimizer_tests.cpp
	optimizer/optimizers/var_def_for_loop_optimizer_tests.cpp
	optimizer/optimizers/var_def_stmt_optimizer_tests.cpp
	optimizer/optimizers/void_return_optimizer_tests.cpp
	optimizer/optimizers/while_true_to_for_loop_optimizer_tests.cpp
	optimizer/optimizers/while_true_to_ufor_loop_optimizer_tests.cpp
	optimizer/optimizers/while_true_to_while_cond_optimizer_tests.cpp
	pattern/pattern_finder_runner_tests.cpp
	pattern/pattern_finder_runners/cli_pattern_finder_runner_tests.cpp
	pattern/pattern_finder_runners/no_action_pattern_finder_runner_tests.cpp
	pattern/pattern_finder_tests.cpp
	pattern/pattern_finders/api_call/api_call_info_seq_parser_tests.cpp
	pattern/pattern_finders/api_call/api_call_info_seq_tests.cpp
	pattern/pattern_finders/api_call/api_call_info_tests.cpp
	pattern/pattern_finders/api_call_pattern_finder_tests.cpp
	pattern/pattern_finders/api_call_seq_pattern_finder_tests.cpp
	pattern/patterns/stmts_pattern_tests.cpp
	semantics/semantics/compound_semantics_tests.cpp
	semantics/semantics/default_semantics_tests.cpp
	semantics/semantics/gcc_general_semantics_tests.cpp
	semantics/semantics/libc_semantics_tests.cpp
	semantics/semantics/win_api_semantics_tests.cpp
	support/const_symbol_converter_tests.cpp
	support/global_vars_sorter_tests.cpp
	support/headers_for_declared_funcs_tests.cpp
	support/library_funcs_remover_tests.cpp
	support/struct_types_sorter_tests.cpp
	support/unreachable_code_in_cfg_remover_tests.cpp
	utils/ir_tests.cpp
	utils/string_tests.cpp
	validator/validators/break_outside_loop_validator_tests.cpp
	validator/validators/no_global_var_def_validator_tests.cpp
	validator/validators/return_validator_tests.cpp
	var_renamer/var_renamer_tests.cpp
	var_renamer/var_renamers/address_var_renamer_tests.cpp
	var_renamer/var_renamers/hungarian_var_renamer_tests.cpp
	var_renamer/var_renamers/readable_var_renamer_tests.cpp
	var_renamer/var_renamers/simple_var_renamer_tests.cpp
	var_renamer/var_renamers/unified_var_renamer_tests.cpp
)

target_include_directories(tests-llvmir2hll
	PRIVATE
		${RETDEC_TESTS_DIR}
)

target_link_libraries(tests-llvmir2hll
	retdec::llvmir2hll
	retdec::utils
	retdec::deps::gmock_main
)

set_target_properties(tests-llvmir2hll
	PROPERTIES
		OUTPUT_NAME "retdec-tests-llvmir2hll"
)

install(TARGETS tests-llvmir2hll
	RUNTIME DESTINATION ${RETDEC_INSTALL_TESTS_DIR}
)
