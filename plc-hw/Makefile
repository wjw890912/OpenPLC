sim_board: sim_uc.sch sim_phys_out.sch sim_ether.sch sim_pwr.sch \
			sim_phys_in.sch packages/* symbols/*
	refdes_renum $^
	gsch2pcb -v -v $^ -o $@

clean:
	rm -f *~ *- *.backup *.new.pcb *.png *.bak *.gbr *.cnc

destroy_pcb: clean
	@bash -c 'echo "Are you sure? cuz this is gonna blow up all your pcb \
	shit."; read answer; if [[ "$$answer" == *yes* ]]; then rm -v -f *.cmd \
	*.pcb *.net; fi'
