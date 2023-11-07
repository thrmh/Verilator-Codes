ifeq ($(VERILATOR_ROOT),)
VERILATOR = verilator
else
export VERILATOR_ROOT
VERILATOR = $(VERILATOR_ROOT)/bin/verilator
endif


default:
	@echo "--Verilator On Off Switch simple example"
	@echo "--VERILATE & BUILD------------------"
	$(VERILATOR) -cc --exe --build -j top.v sim_main.cpp
	@echo "---RUN------------------------------"
	obj_dir/Vtop
	@echo "---DONE-----------------------------"

maintainer-copy::
clean mostlyclean distclean maintainer-clean:
	-rm -rf obj_dir *.log *.dmp *.vpd core
